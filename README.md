# Sequential Cohort Selection under Uncertainty

This repository contains the official implementation accompanying our paper on adaptive policy learning for sequential university admissions under uncertainty.

The project studies cohort selection as a sequential decision-making problem in which admission policies are optimized to maximize expected utility while accounting for uncertainty in applicant outcomes. We consider both a **one-shot** setting, where a policy is learned once and evaluated on unseen applicants, and a **multi-stage** setting, where admission policies are continuously refined over successive admission cycles using newly observed outcomes.

Our framework combines probabilistic outcome modeling, policy gradient optimization, and generative modeling to learn admission policies from partially observed data.


## Features

* Policy gradient optimization for admission decisions
* Logistic and neural network admission policies
* Bayesian multivariate linear regression for outcome prediction
* Thompson Sampling for sequential policy learning
* CTGAN-based applicant population modeling
* One-shot and multi-stage admission settings
* Utility-based policy optimization with admission cost
* Fairness evaluation using Demographic Parity and Equality of Opportunity
* Baseline comparisons against threshold-based and greedy admission strategies


## Repository Structure

The repository is organized into independent modules corresponding to the main components of the proposed framework, including data preprocessing, policy optimization, utility computation, fairness evaluation, baseline methods, and experimental notebooks used to reproduce the results reported in the paper.

```text
├── ecaf.ipynb                         # Main notebook used for experiments and figures
├── single_stage_policy_gradient.py    # Policy gradient algorithm for the one-shot setting
├── multistage.py                      # Sequential (multi-stage) policy learning framework
├── policies.py                        # Logistic and neural network admission policies
├── probability_distribution.py        # Bayesian outcome model and probability distribution utilities
├── expected_utilities.py              # Expected utility computation and optimization objective
├── fairness_metric.py                 # Fairness metrics (Demographic Parity and Equality of Opportunity)
├── baseline.py                        # Threshold-based and greedy baseline methods
├── data_preprocessing.py              # Data preprocessing and feature engineering
├── admitted_students.csv              # Historical admitted-student dataset
├── generated_data.csv                 # Synthetic applicant dataset
└── README.md                          # Project documentation
```

## Installation

```bash
git clone https://github.com/phalonneNana/European-Conference-on-Algorithmic-Fairness-26.git
cd European-Conference-on-Algorithmic-Fairness-26

pip install -r requirements.txt
```

If a `requirements.txt` file is not available, install the required Python packages listed in `data_preprocessing.py`.
