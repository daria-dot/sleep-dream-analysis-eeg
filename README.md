# sleep-dream-analysis-eeg
classification of the dream cycle from an EEG dataset, as well as anomaly detection
│
├── /data/                  # Raw and processed data ( .gitignore to avoid pushing large files)
│   ├── /raw/               # Raw data files (EEG signals from Kaggle )
│   ├── /processed/         # Preprocessed data (
features, segmented data)
│   └── README.md           # Instructions for dataset usage and preprocessing steps
│
├── /notebooks/             # Jupyter notebooks for exploration, analysis, and prototyping
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_extraction.ipynb
│   ├── 03_model_training.ipynb
│   └── 04_model_evaluation.ipynb
│
├── /src/                   # Source code for the project
│   ├── /preprocessing/     # Scripts for data preprocessing
│   │   ├── filter_data.py  # Filtering EEG signals
│   │   ├── extract_features.py  # Feature extraction (e.g., PSD, wavelet)
│   │   └── segment_data.py   # Segmenting EEG into epochs
│   ├── /model/             # Model building and training scripts
│   │   ├── train_model.py   # Training the ML model
│   │   ├── evaluate_model.py # Evaluate the trained model
│   │   └── anomaly_detection.py # Anomaly detection (e.g., insomnia)
│   └── /utils/             # Utility functions (e.g., data loading, evaluation metrics)
│       └── helpers.py
│
├── /docker/                # Docker-related files for deployment
│   ├── Dockerfile          # Dockerfile to containerize the project
│   └── /app/               # FastAPI or Flask app for serving the model
│       ├── main.py         # FastAPI app entry point
│       └── requirements.txt  # Dependencies for the API
│
├── /models/                # Trained machine learning models (e.g., .h5 files)
│   └── model.h5            # Trained model file (e.g., LSTM or Autoencoder)
│
├── /results/               # Results (e.g., plots, evaluation metrics, logs)
│   ├── /plots/             # Plots of model performance, feature importance, etc.
│   ├── evaluation_metrics.txt  # Performance evaluation results (accuracy, loss, etc.)
│   └── logs/               # Logs from training and evaluation
│
├── .gitignore              # To ignore unnecessary files (e.g., large data files, .h5 models)
├── README.md               # Project overview, setup instructions, usage
└── requirements.txt        # Python dependencies for the project
