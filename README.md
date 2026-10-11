# AI-Powered Telecom Customer Churn Analytics

Analyze telecom customer churn patterns and estimate churn risk with logistic regression and random forest using IBM’s public sample dataset.

## Dataset
- IBM CSV: https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
- IBM repository: https://github.com/IBM/telco-customer-churn-on-icp4d

The notebook downloads the CSV when run. For offline use, download it and set `DATA_PATH` in the notebook to the local CSV path.

## Submission files
- `PraneetVerma_TelcoCustomerChurnAnalytics.ipynb` — complete analysis and modeling notebook
- `requirements.txt` — required Python dependencies
- `PraneetVerma_ProjectReport.docx` — project report
- `README.md` — overview and run instructions

## Technologies
Python, Jupyter, pandas, NumPy, Matplotlib, Seaborn, and scikit-learn.

## Run in VS Code
1. Install Python 3.10 or later.
2. Install the Python and Jupyter extensions in VS Code.
3. Open a terminal in the project folder and run `python -m pip install -r requirements.txt`.
4. Open `PraneetVerma_TelcoCustomerChurnAnalytics.ipynb`, select the environment/kernel where dependencies are installed, and choose **Run All**.

You can also run it with JupyterLab. Internet access is needed to download the dataset unless `DATA_PATH` points to a local CSV.

## Project question and interpretation
Can customer attributes and subscribed services help identify customers at elevated risk of leaving? The notebook compares models using held-out ROC-AUC, average precision, precision, recall, F1, and a confusion matrix. The 0.50 classification threshold is illustrative. This sample is educational: predictions and feature importance do not prove causes or guarantee outcomes. Validate performance, fairness, privacy, and decision thresholds before operational use. Run the notebook and add the observed metrics to the report before submission.
