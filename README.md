# Income Prediction

A machine learning project that predicts whether a person's annual income is above or below **$50,000** from census-style demographic and employment data. The task is a binary classification problem.

## Project goals

- Prepare and validate input data before model training or prediction.
- Train classification models to estimate the income class.
- Support prediction workflows using batch files and database-backed input.
- Keep logs and invalid records available for troubleshooting.

## Repository structure

| Path | Purpose |
| --- | --- |
| `main.py` | Application entry point |
| `trainingModel.py` | Model training workflow |
| `training_Validation_Insertion.py` | Training data validation and insertion workflow |
| `prediction_Validation_Insertion.py` | Prediction data validation and insertion workflow |
| `predictFromModel.py` | Prediction using the trained model |
| `schema_training.json` | Expected training data schema |
| `schema_prediction.json` | Expected prediction data schema |
| `data/` | Project data files |
| `models/` | Model artifacts |
| `templates/` | Web interface templates |
| `application_logging/` | Logging utilities or logs |
| `Training_*` | Training data validation, transformation, ingestion, and logs |
| `Prediction_*` | Prediction data validation, transformation, ingestion, and logs |
| `requirements.txt` | Python dependencies |
| `Procfile`, `manifest.yml`, `runtime.txt` | Deployment/runtime configuration files |

> Directory and file names above describe the repository layout. For exact behavior, review the corresponding source files and configuration.

## Machine learning approach

The project frames income estimation as a classification task: predict one of two classes, **income above $50K** or **income at or below $50K**. Classification experiments include Random Forest and XGBoost. Confirm the final selected model and evaluation results from the training code and run output before adding exact scores.

## Technologies

- Python
- Machine learning and data processing libraries listed in `requirements.txt`
- Schema-based input validation
- Batch/file and database-oriented data workflows
- Logging

## Getting started

Use a supported Python version for the project and create an isolated environment:

```bash
python -m venv .venv
```

Activate it, then install the project dependencies:

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

python -m pip install -r requirements.txt
```

Check the source files and deployment configuration for the expected database settings, input-file locations, and application start command before running the pipeline. Do not commit credentials or private data to the repository.

## Input data

Use data that matches the fields and types defined in `schema_training.json` for training, and `schema_prediction.json` for prediction. Check the repository's data-handling and validation modules for required columns and accepted values.

## Results and evaluation

Evaluate the trained classifier on data that was held out from training. Report appropriate classification metrics such as precision, recall, F1-score, and a confusion matrix, especially if the income classes are imbalanced. No metric values are included here because the repository overview does not establish verified results.

## Limitations

- Predictions reflect patterns in the source dataset and may not generalize to other populations, locations, or time periods.
- Demographic and employment attributes can encode historical bias. Treat outputs as experimental estimates, not decisions about an individual.
- Model performance and data quality should be checked before any real-world use.

## Author

**Kunal Suryawanshi**

- GitHub: [kunalsuryawanshi161718](https://github.com/kunalsuryawanshi161718)
- Project: [Income_prediction](https://github.com/kunalsuryawanshi161718/Income_prediction)

## License

No license information was visible in the repository overview. Add a `LICENSE` file and update this section before redistributing or reusing the project.
