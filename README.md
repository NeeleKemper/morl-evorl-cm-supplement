# Comparative Analysis of Multi-Objective and Evolutionary Reinforcement Learning Algorithms in Electric Vehicle Charging Management - Extended Appendix
## Appendix: Simulation
### PV Power Curve
![](plots/pv.png)

*PV Power Curve: Hourly average power of the PV system over a recorded one-year period.*

## Appendix: Hyperparameter Optimization Results
| Parameter           | Distribution | Min         | Max         |
|---------------------|--------------|-------------|-------------|
| sbx_prob            | uniform      | 0.6         | 0.95        |
| mut_prob            | uniform      | 0.1         | 0.3         |
| sbx_eta             | int_uniform  | 3           | 30          |
| mut_eta             | int_uniform  | 3           | 30          |
| net_arch            | categorical  | [32, 32], [32, 32, 32], [32, 32, 32, 32] | - |
| batch_size          | categorical  | 8, 16, 32   | -           |
| env_iterations      | categorical  | 2, 5, 10    | -           |
| pop_size            | fixed        | 200         | -           |
| activation_function | fixed        | sigmoid     | -           |

*MOEvoRL-NSGA-II and MOEvoRL-SPEA2 Hyperparameter Search Space: The hyperparameter search space for the MOEvoRL-NSGA-II and MOEvoRL-SPEA2 agents.*

| Parameter                  | Distribution | Min   | Max   |
|----------------------------|--------------|-------|-------|
| conn_add_prob              | uniform      | 0.6   | 0.9   |
| conn_delete_prob           | uniform      | 0.1   | 0.4   |
| node_add_prob              | uniform      | 0.6   | 0.9   |
| node_delete_prob           | uniform      | 0.1   | 0.4   |
| survival_threshold         | uniform      | 0.1   | 0.3   |
| aggregation_mutate_rate    | uniform      | 0.1   | 0.3   |
| weight_mutate_rate         | uniform      | 0.6   | 0.9   |
| bias_mutate_rate           | uniform      | 0.6   | 0.9   |
| batch_size                 | categorical  | 8, 16, 32 | -    |
| env_iterations             | categorical  | 2, 5, 10  | -    |
| pop_size                   | fixed        | 200       | -    |
| activation_function        | fixed        | sigmoid   | -    |


*MOEvoRL-FF-NEAT and MOEvoRL-RNN-NEAT Hyperparameter Search Space: The hyperparameter search space for the MOEvoRL-FF-NEAT agents.*

| Parameter                    | Distribution | Min                   | Max                  |
|------------------------------|--------------|-----------------------|----------------------|
| gamma                        | uniform      | 0.95                  | 0.9999               |
| tau                          | uniform      | 0                     | 0.1                  |
| per_alpha                    | uniform      | 0.1                   | 1.0                  |
| learning_rate                | uniform      | \(1 \times 10^{-5}\)  | \(1 \times 10^{-4}\) |
| learning_starts              | int_uniform  | 1000                  | 10000                |
| policy_frequency             | int_uniform  | 1                     | 20                   |
| buffer_size                  | int_uniform  | \(1 \times 10^5\)     | \(2 \times 10^6\)    |
| batch_size                   | categorical  | 128, 256, 512         | -                    |
| net_arch                     | fixed        | [1024, 1024, 1024]    | -                    |
| activation_function          | fixed        | relu                  | -                    |
| output_activation_function   | fixed        | tanh                  | -                    |
| optimizer                    | fixed        | adam                  | -                    |

*MOODPG Hyperparameter Search Space: The hyperparameter search space for the MODDPG agents*

### MOEvoRL-NSGA-II Optimal Hyperparameters

| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.90         |
| mut_prob                 | 0.18         |
| sbx_eta                  | 23           |
| mut_eta                  | 22           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 32           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-NSGA-II CS05-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.75         |
| mut_prob                 | 0.26         |
| sbx_eta                  | 23           |
| mut_eta                  | 12           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 16           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-NSGA-II CS05-Med-AR-42: Best hyperparameter parameter configuration.*


| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.83         |
| mut_prob                 | 0.29         |
| sbx_eta                  | 26           |
| mut_eta                  | 27           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 16           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-NSGA-II CS10-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.74         |
| mut_prob                 | 0.14         |
| sbx_eta                  | 19           |
| mut_eta                  | 15           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 8           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-NSGA-II CS10-Med-AR-42: Best hyperparameter parameter configuration.*


### MOEvoRL-SPEA2 Optimal Hyperparameters

| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.88         |
| mut_prob                 | 0.21        |
| sbx_eta                  | 16           |
| mut_eta                  | 24           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 32           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-SPEA2 CS05-Med-42: Best hyperparameter parameter configuration.*

| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.76         |
| mut_prob                 | 0.20        |
| sbx_eta                  | 16           |
| mut_eta                  | 12           |
| net_arch                 | [32, 32, 32, 32] |
| batch_size               | 16           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-SPEA2 CS05-Med-AR-42: Best hyperparameter parameter configuration.*


| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.82         |
| mut_prob                 | 0.28        |
| sbx_eta                  | 14           |
| mut_eta                  | 8           |
| net_arch                 | [32, 32, 32] |
| batch_size               | 32           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-SPEA2 CS10-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**            | **Value**    |
|--------------------------|--------------|
| sbx_prob                 | 0.85         |
| mut_prob                 | 0.22        |
| sbx_eta                  | 18           |
| mut_eta                  | 13           |
| net_arch                 | [32, 32, 32, 32] |
| batch_size               | 16           |
| env_iterations           | 10           |
| pop_size                 | 200          |
| activation_function      | sigmoid      |

*MOEvoRL-SPEA2 CS10-Med-AR-42: Best hyperparameter parameter configuration.*


### MOEvoRL-FF-NEAT Optimal Hyperparameters

| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.72      |
| conn_delete_prob             | 0.25      |
| node_add_prob                | 0.60      |
| node_delete_prob             | 0.28      |
| survival_threshold           | 0.20      |
| aggregation_mutate_rate      | 0.22      |
| weight_mutate_rate           | 0.89      |
| bias_mutate_rate             | 0.64      |
| batch_size                   | 32        |
| env_iterations               | 10        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-FF-NEAT CS05-Med-42: Best hyperparameter parameter configuration.*



| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.73      |
| conn_delete_prob             | 0.39      |
| node_add_prob                | 0.79      |
| node_delete_prob             | 0.32      |
| survival_threshold           | 0.12      |
| aggregation_mutate_rate      | 0.20      |
| weight_mutate_rate           | 0.71      |
| bias_mutate_rate             | 0.79      |
| batch_size                   | 8        |
| env_iterations               | 2        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-FF-NEAT CS05-Med-AR-42: Best hyperparameter parameter configuration.*


| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.79      |
| conn_delete_prob             | 0.33      |
| node_add_prob                | 0.70      |
| node_delete_prob             | 0.28      |
| survival_threshold           | 0.16      |
| aggregation_mutate_rate      | 0.26      |
| weight_mutate_rate           | 0.65      |
| bias_mutate_rate             | 0.66      |
| batch_size                   | 16        |
| env_iterations               | 10        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-FF-NEAT CS10-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.82      |
| conn_delete_prob             | 0.18      |
| node_add_prob                | 0.67      |
| node_delete_prob             | 0.31      |
| survival_threshold           | 0.23      |
| aggregation_mutate_rate      | 0.26      |
| weight_mutate_rate           | 0.74      |
| bias_mutate_rate             | 0.84      |
| batch_size                   | 16        |
| env_iterations               | 10        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-FF-NEAT CS10-Med-AR-42: Best hyperparameter parameter configuration.*


### MOEvoRL-RNN-NEAT Optimal Hyperparameters

| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.72      |
| conn_delete_prob             | 0.35      |
| node_add_prob                | 0.66      |
| node_delete_prob             | 0.16      |
| survival_threshold           | 0.17      |
| aggregation_mutate_rate      | 0.24      |
| weight_mutate_rate           | 0.81      |
| bias_mutate_rate             | 0.78      |
| batch_size                   | 32        |
| env_iterations               | 5        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-RNN-NEAT CS05-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.83      |
| conn_delete_prob             | 0.39      |
| node_add_prob                | 0.84      |
| node_delete_prob             | 0.39      |
| survival_threshold           | 0.27      |
| aggregation_mutate_rate      | 0.23      |
| weight_mutate_rate           | 0.87      |
| bias_mutate_rate             | 0.85      |
| batch_size                   | 8        |
| env_iterations               | 5        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-RNN-NEAT CS05-Med-AR-42: Best hyperparameter parameter configuration.*


| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.76      |
| conn_delete_prob             | 0.24      |
| node_add_prob                | 0.77      |
| node_delete_prob             | 0.25      |
| survival_threshold           | 0.21      |
| aggregation_mutate_rate      | 0.29      |
| weight_mutate_rate           | 0.85      |
| bias_mutate_rate             | 0.66      |
| batch_size                   | 32        |
| env_iterations               | 10        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-RNN-NEAT CS10-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**                | **Value** |
|------------------------------|-----------|
| conn_add_prob                | 0.75      |
| conn_delete_prob             | 0.15      |
| node_add_prob                | 0.75      |
| node_delete_prob             | 0.20      |
| survival_threshold           | 0.23      |
| aggregation_mutate_rate      | 0.24      |
| weight_mutate_rate           | 0.80      |
| bias_mutate_rate             | 0.67      |
| batch_size                   | 32        |
| env_iterations               | 10        |
| pop_size                     | 200       |
| activation_function          | sigmoid   |

*MOEvoRL-RNN-NEAT CS10-Med-AR-42: Best hyperparameter parameter configuration.*



### MODDPG Optimal Hyperparameters
| **Parameter**                   | **Value**             |
|---------------------------------|-----------------------|
| gamma                           | 0.99                  |
| tau                             | 0.04                  |
| per_alpha                       | 0.71                  |
| learning_rate                   | 1.1 x 10^{-5}         |
| learning_starts                 | 7500                  |
| policy_frequency                | 13                    |
| buffer_size                     | $1 x 10^6$            |
| batch_size                      | 256                   |
| net_arch                        | [1024, 1024, 1024]    |
| activation_function             | relu                  |
| output_activation_function      | tanh                  |
| optimizer                       | adam                  |

*MODDPG CS05-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**                   | **Value**             |
|---------------------------------|-----------------------|
| gamma                           | 0.99                  |
| tau                             | 0.09                  |
| per_alpha                       | 0.60                  |
| learning_rate                   | 1.8 x 10^{-5}         |
| learning_starts                 | 1500                  |
| policy_frequency                | 6                    |
| buffer_size                     | $1 x 10^6$            |
| batch_size                      | 256                   |
| net_arch                        | [1024, 1024, 1024]    |
| activation_function             | relu                  |
| output_activation_function      | tanh                  |
| optimizer                       | adam                  |

*MODDPG CS05-Med-AR-42: Best hyperparameter parameter configuration.*


| **Parameter**                   | **Value**             |
|---------------------------------|-----------------------|
| gamma                           | 0.99                  |
| tau                             | 0.02                  |
| per_alpha                       | 0.65                  |
| learning_rate                   | 6.2 x 10^{-5}         |
| learning_starts                 | 9100                  |
| policy_frequency                | 6                    |
| buffer_size                     | $1 x 10^6$            |
| batch_size                      | 512                   |
| net_arch                        | [1024, 1024, 1024]    |
| activation_function             | relu                  |
| output_activation_function      | tanh                  |
| optimizer                       | adam                  |

*MODDPG CS10-Med-42: Best hyperparameter parameter configuration.*


| **Parameter**                   | **Value**             |
|---------------------------------|-----------------------|
| gamma                           | 0.99                  |
| tau                             | 0.04                  |
| per_alpha                       | 0.80                  |
| learning_rate                   | 8.6 x 10^{-5}         |
| learning_starts                 | 5600                  |
| policy_frequency                | 16                    |
| buffer_size                     | $1 x 10^6$            |
| batch_size                      | 128                   |
| net_arch                        | [1024, 1024, 1024]    |
| activation_function             | relu                  |
| output_activation_function      | tanh                  |
| optimizer                       | adam                  |

*MODDPG CS10-Med-AR-42: Best hyperparameter parameter configuration.*


## Appendix: Anaylsis of Charging Events
### CS05 Charging Events
![](plots/charging_events/scenario_CS05_distribution_med_42.png)

*Arrival and Charging Patterns for CS05-Med-42*

![](plots/charging_events/scenario_CS05_distribution_low_71.png)

*Arrival and Charging Patterns for CS05-Low-71*

![](plots/charging_events/scenario_CS05_distribution_med_71.png)

*Arrival and Charging Patterns for CS05-Med-71*

![](plots/charging_events/scenario_CS05_distribution_high_71.png)

*Arrival and Charging Patterns for CS05-High-71*

![](plots/charging_events/scenario_CS05_car_count_med_42.png)

*EV Model Distribution in CS05-Med-42*

![](plots/charging_events/scenario_CS05_car_count_low_71.png)

*EV Model Distribution in CS05-Low-71*

![](plots/charging_events/scenario_CS05_car_count_med_71.png)

*EV Model Distribution in CS05-Med-71*

![](plots/charging_events/scenario_CS05_car_count_high_71.png)

*EV Model Distribution in CS05-High-71*

### CS10 Charging Events
![](plots/charging_events/scenario_CS10_distribution_med_42.png)

*Arrival and Charging Patterns for CS10-Med-42*

![](plots/charging_events/scenario_CS10_distribution_low_71.png)

*Arrival and Charging Patterns for CS10-Low-71*

![](plots/charging_events/scenario_CS10_distribution_med_71.png)

*Arrival and Charging Patterns for CS10-Med-71*

![](plots/charging_events/scenario_CS10_distribution_high_71.png)

*Arrival and Charging Patterns for CS10-High-71*

![](plots/charging_events/scenario_CS10_car_count_med_42.png)

*EV Model Distribution in CS10-Med-42*

![](plots/charging_events/scenario_CS10_car_count_low_71.png)

*EV Model Distribution in CS10-Low-71*

![](plots/charging_events/scenario_CS10_car_count_med_71.png)

*EV Model Distribution in CS10-Med-71*

![](plots/charging_events/scenario_CS10_car_count_high_71.png)

*EV Model Distribution in CS10-High-71*


## Appendix: Comparative Analysis of Training Dynamics
### CS05-Med-42 Training Performance

![](plots/training/scenario_0a_r0_comparison.png)

*R0 Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the reward R0 throughout the training episodes.*


![](plots/training/scenario_0a_r1_comparison.png)

*R1 Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the reward R1 throughout the training episodes.*


![](plots/training/scenario_0a_r2_comparison.png)

*R2 Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the reward R2 throughout the training episodes.*


![](plots/training/scenario_0a_success_rate_comparison.png)

*Success Rate Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the Success Rate throughout the training episodes.*

![](plots/training/scenario_0a_hypervolume_comparison.png)

*Hypervolume Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the HV throughout the training episodes.*

![](plots/training/scenario_0a_sparsity_comparison.png)

*Sparsity Comparison CS05-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-42, focusing on the Sparsity throughout the training episodes.*

### CS05-Med-AR-42 Training Performance

![](plots/training/scenario_0b_r0_comparison.png)

*R0 Comparison CS05-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-AR-42, focusing on the reward R0 throughout the training episodes.*


![](plots/training/scenario_0b_r1_comparison.png)

*R1 Comparison CS05-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-AR-42, focusing on the reward R1 throughout the training episodes.*


![](plots/training/scenario_0b_r2_comparison.png)

*R2 Comparison CS05-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-AR-42, focusing on the reward R2 throughout the training episodes.*

![](plots/training/scenario_0b_hypervolume_comparison.png)

*Hypervolume Comparison CS05-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-AR-42, focusing on the HV throughout the training episodes.*

![](plots/training/scenario_0b_sparsity_comparison.png)

*Sparsity Comparison CS05-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS05-Med-AR-42, focusing on the Sparsity throughout the training episodes.*


### CS10-Med-42 Training Performance

![](plots/training/scenario_1a_r0_comparison.png)

*R0 Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the reward R0 throughout the training episodes.*


![](plots/training/scenario_1a_r1_comparison.png)

*R1 Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the reward R1 throughout the training episodes.*


![](plots/training/scenario_1a_r2_comparison.png)

*R2 Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the reward R2 throughout the training episodes.*


![](plots/training/scenario_1a_success_rate_comparison.png)

*Success Rate Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the Success Rate throughout the training episodes.*

![](plots/training/scenario_1a_hypervolume_comparison.png)

*Hypervolume Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the HV throughout the training episodes.*

![](plots/training/scenario_1a_sparsity_comparison.png)

*Sparsity Comparison CS10-Med-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-42, focusing on the Sparsity throughout the training episodes.*

### CS10-Med-AR-42 Training Performance

![](plots/training/scenario_1b_r0_comparison.png)

*R0 Comparison CS10-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-AR-42, focusing on the reward R0 throughout the training episodes.*


![](plots/training/scenario_1b_r1_comparison.png)

*R1 Comparison CS10-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-AR-42, focusing on the reward R1 throughout the training episodes.*


![](plots/training/scenario_1b_r2_comparison.png)

*R2 Comparison CS10-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-AR-42, focusing on the reward R2 throughout the training episodes.*

![](plots/training/scenario_1b_hypervolume_comparison.png)

*Hypervolume Comparison CS10-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-AR-42, focusing on the HV throughout the training episodes.*

![](plots/training/scenario_1b_sparsity_comparison.png)

*Sparsity Comparison CS10-Med-AR-42: Diagram provides a comparative analysis of the convergence behavior of five models in scenario CS10-Med-AR-42, focusing on the Sparsity throughout the training episodes.*

