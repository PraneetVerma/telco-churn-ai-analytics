# AI-Powered Telecom Customer Churn Analytics

An end-to-end data analytics and AI project that explores telecom churn patterns and estimates churn risk using Logistic Regression and Random Forest.

## Dataset
- IBM Telco Customer Churn CSV: https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
- IBM source repository: https://github.com/IBM/telco-customer-churn-on-icp4d

The notebook downloads the CSV at runtime. For offline use, download the file and set `DATA_PATH` in the notebook to its local path.

## Project files
- `PraneetVerma_TelcoCustomerChurnAnalytics.ipynb` — analysis, visualizations, model training, and evaluation (executed with outputs)
- `requirements.txt` — Python dependencies
- `PraneetVerma_ProjectReport.docx` — report with results from the executed notebook
- `README.md` — project overview and run instructions

## Technologies
Python, Jupyter/VS Code notebooks, pandas, NumPy, Matplotlib, Seaborn, and scikit-learn.

## Run in VS Code
1. Install Python 3.10+ and the VS Code **Python** and **Jupyter** extensions.
2. Open a terminal in the project folder and install dependencies: `python -m pip install -r requirements.txt`.
3. Open `PraneetVerma_TelcoCustomerChurnAnalytics.ipynb`, select the Python environment where dependencies were installed, then choose **Run All**.

Internet is needed for the default dataset download. To use JupyterLab instead, install it separately with `python -m pip install jupyterlab`.

## Results from the executed run
The model was selected using mean 5-fold stratified cross-validation ROC-AUC on the training data; the stratified 20% holdout was reserved for final evaluation. With random seed 42, Logistic Regression was selected (training CV ROC-AUC **0.846**). On the test holdout it achieved ROC-AUC **0.841**, average precision **0.633**, precision **0.504**, recall **0.783**, F1 **0.614**, and accuracy **0.738** at the illustrative 0.50 threshold. Random Forest test ROC-AUC was 0.837, average precision 0.641, precision 0.534, recall 0.743, F1 0.621, and accuracy 0.759.

Tenure, InternetService, Contract, and MonthlyCharges were the leading permutation-importance features for the selected model in this run. Predictive associations and feature importance do not establish causes. The threshold is illustrative; validate fairness, privacy, calibration, temporal performance, and business costs before operational use.
