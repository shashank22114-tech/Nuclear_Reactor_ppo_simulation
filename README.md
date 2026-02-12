 # Autonomous Nuclear Reactor Control using PPO Reinforcement Learning

  ## Overview
  This project simulates a nuclear reactor core using **6-group point kinetics with delayed neutron precursors** and trains a **Proximal Policy Optimization (PPO)** reinforcement learning agent to autonomously maintain the reactor at **100% power** under strict safety constraints.

  The environment integrates realistic reactor physics, thermal feedback, and control actions.  
  The trained agent learns to stabilize reactor power without triggering SCRAM shutdown conditions, demonstrating reinforcement learning applied to a **safety-critical control system**.

  This project showcases advanced reinforcement learning, physics-informed simulation, and autonomous control.

  ---

  ## Key Features
  - 6-group delayed neutron point-kinetics reactor model  
  - thermal-hydraulic coupling  
  - Doppler & moderator feedback  
  - control rod reactivity modeling  
  - coolant flow dynamics  
  - PPO actor-critic implementation  
  - safety SCRAM logic  
  - robust normalization & gradient clipping  
  - closed-loop autonomous reactor control  

  ---

  ## Physics Model

  The reactor core simulation includes:

  **State variables**
  - Reactor power (neutron population)
  - Delayed neutron precursor concentration
  - Fuel temperature
  - Coolant temperature

  **Reactivity sources**
  - Control rod insertion
  - Doppler fuel temperature feedback
  - Moderator/coolant temperature feedback

  **Safety constraints**
  - SCRAM if power < 50%
  - SCRAM if power > 200%

  **Target operating point**
      100% reactor power

  ---

  ## Reinforcement Learning Setup

  **Algorithm:** Proximal Policy Optimization (PPO)

  **Observation space**
      [Power, Avg Precursors, Fuel Temp, Coolant Temp]

  **Action space**
      Control rod movement  
      Coolant flow rate

  **Reward function**
  - High reward for maintaining 100% power
  - Penalty for deviation from target
  - Heavy penalty for SCRAM shutdown

  ---

  ## Training Configuration
  - Episodes: 100  
  - Simulation length per episode: 20 seconds  
  - Time step: 0.01 s  
  - Actor-critic neural network  
  - Observation normalization  
  - Gradient clipping  
  - Entropy regularization  

  The agent learns stable control behavior across episodes.

  ---

  ## Results

  After training, the agent:
  - Maintains reactor power near 1.0  
  - Avoids SCRAM conditions  
  - Stabilizes fuel temperature  
  - Demonstrates closed-loop autonomous control
  - 
  ---

  ## Technical Highlights
  - PPO implementation from scratch  
  - Physics-informed RL environment  
  - Safety-critical control system  
  - Numerical stability handling  
  - Custom reward shaping  
  - Actor-critic architecture  

  ---

  ## Potential Extensions
  - Multi-reactor grid control
  - Real-time dashboard
  - Model predictive control hybrid
  - Domain randomization
  - Web-based visualization

  ---

  ## Author
  Shashank Reddy  
  B.Tech Computer Science  
  GitHub: https://github.com/yourusername
