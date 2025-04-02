meta_continual_learning/
│
├── README.md                        # Project documentation
├── requirements.txt                 # Dependencies
├── setup.py                         # Package setup
├── .gitignore                       # Git ignore file
│
├── config/                          # Configuration files
│   ├── __init__.py
│   ├── base_model_config.yaml       # Base model parameters
│   ├── verifier_config.yaml         # Verifier model parameters
│   └── experiment_config.yaml       # Overall experiment settings
│
├── data/                            # Data management
│   ├── __init__.py
│   ├── synthetic_data_generator.py  # Generate synthetic training data
│   ├── task_stream.py               # Create continuous task streams
│   └── data_utils.py                # Utilities for data processing
│
├── models/                          # Model definitions
│   ├── __init__.py
│   ├── base_model.py                # Base language model to be updated
│   ├── verifier.py                  # Verifier model architecture
│   └── weight_encoder.py            # Process weight deltas for the verifier
│
├── training/                        # Training loop implementations
│   ├── __init__.py
│   ├── base_model_trainer.py        # Train the base language model
│   ├── verifier_offline_trainer.py  # Initial training of verifier
│   ├── verifier_online_trainer.py   # Continual training of verifier
│   ├── ewc.py                       # Elastic Weight Consolidation implementation
│   └── si.py                        # Synaptic Intelligence implementation
│
├── evaluation/                      # Metrics and evaluation
│   ├── __init__.py
│   ├── verifier_metrics.py          # Evaluate verifier performance
│   ├── model_performance.py         # Evaluate base model performance
│   ├── drift_analysis.py            # Analyze verifier drift over time
│   └── visualization.py             # Visualization utilities
│
├── utils/                           # Utility functions
│   ├── __init__.py
│   ├── logging_utils.py             # Logging utilities
│   ├── weight_utils.py              # Weight management utilities
│   └── experiment_tracker.py        # Track experiment progress
│
└── experiments/                     # Experiment scripts
    ├── __init__.py
    ├── phase1_offline_training.py   # Phase 1: Initial verifier training
    ├── phase2_online_training.py    # Phase 2: Live continual training
    ├── baseline_ewc.py              # EWC baseline
    ├── baseline_si.py               # SI baseline
    └── run_experiment.py            # Main experiment runner