# Bank-Queue-Simulation-and-Optimization

### Objective:
Simulate and evaluate the performance of a bank’s queuing system using discrete-event simulation in R.

### Tools & Libraries Used:
Utilized `simmer`, `simmer.plot`, `ggplot2`, and `dplyr` in R for simulation, visualization, and data analysis.

#### Model Setup:

Assumed M/M/c queuing model with Poisson arrivals and exponential service times.

Simulated for an 8-hour (480-minute) business day.

Parameters: 
- λ = 10 customers/hour
- μ = 1 customer/5 minutes.

#### Simulated Scenarios:

1 Counter: 
- High waiting time and queue length; max wait = 34.21 min; utilization = 78.85%.

2 Counters (Current): 
- Balanced performance; avg wait = 1.10 min; utilization = 43.06%.

3 Counters: 
- Minimal waiting; avg wait = 0.08 min; underutilization at 27.43%.

#### Performance Metrics Calculated:

- Customers served

- Average queue length

- Average & max waiting time

- Server utilization

- Theoretical vs. Simulated Comparison:

- M/M/2 theory matched closely with simulated metrics (Wq theoretical = 1.05 min vs. simulated = 1.10 min).

#### Visual Analysis:

- Histograms of waiting time distribution for each scenario.

- Queue evolution graphs over time.

- Server utilization and throughput bar charts.

- Convergence graph showing average waiting time over extended simulation duration.

#### Key Findings:

- 2-counter system offers an optimal trade-off between service quality and resource use.

- 3-counter setup reduces waiting but is economically inefficient.

- 1-counter system is overburdened and results in customer dissatisfaction.

### Conclusion:
*Recommend maintaining 2 counters for typical business hours. Consider dynamic scaling (adding a third counter during peak demand) for cost-effective service improvements.*
