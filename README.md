# Report  
## Policy Gradient  
### Baseline
- [x] Getting averaging reward in 30 episodes over 0 in LunarLander

###   structure 1
```python
nn.Sequential(
    nn.Linear(state_dim, hidden_dim),
    nn.ReLU(),
    nn.Linear(hidden_dim, hidden_dim),
    nn.ReLU(),
    nn.Linear(hidden_dim, action_num),
    nn.Softmax(dim=-1)
)
```
*   Testing  (pg_best.cpt)  
Run 30 episodes  
Mean: 196.97405585001098

*  training curve
![](https://i.imgur.com/TBSnXqJ.png) 

### Result

<details><summary>CLICK ME</summary>
<p>

<img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/pg_1.gif" width="40%"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/pg_2.gif" width="40%">

<img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/pg3.gif" width="40%"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/pg4.gif" width="40%">

</p>
</details>




## 2. DQN

### 2.1 baseline
- [x] Getting averaging reward in 100 episodes over 100 in Assault
- [x] Improvements to DQN are allowed, not including Actor-Critic series.

structure  
```python
self.conv1 = nn.Conv2d(channels, 32, kernel_size=8, stride=4)
self.conv2 = nn.Conv2d(32, 64, kernel_size=4, stride=2)
self.conv3 = nn.Conv2d(64, 64, kernel_size=3, stride=1)
self.fc = nn.Linear(3136, 512)
self.lrelu = nn.LeakyReLU(0.01)
self.head = nn.Linear(512, num_actions)
```
### Testing   
#### DQN :  
Run 100 episodes    
Mean: 222.8  
![](https://i.imgur.com/hSgpZQ0.png)
#### Dueling DQN:  
Run 100 episodes  
Mean: 366.17  
![](https://i.imgur.com/bu6rw4A.png)


### Result

<details><summary>CLICK ME</summary>
<p>

<img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/dqn_1.gif" width="25%"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/dqn_2.gif" width="25%"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/dqn_3.gif" width="25%"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/dqn_4.gif" width="25%">

</p>
</details>

## 3. Mario
- [x] Getting averaging reward in 10 episodes over 1500 in SuperMarioBros
- [ ] Getting averaging reward in 10 episodes over 3000 in SuperMarioBros
### Testing
Run 10 episodes  
Mean: 1881.490000000026  
![](https://i.imgur.com/Nwm96Ze.png)


### Result

<details><summary>CLICK ME</summary>
<p>

<img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/ac_1.gif"><img src="https://github.com/tommyvsfu1/ADL2019_rl/blob/master/result/ac_2.gif">

</p>
</details>
