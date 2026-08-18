# sirius-ml-intro-project-1
Flight satisfaction prediction. Sirius Courses — Introduction to ML. A simple ML project to predict passenger satisfaction using a CSV dataset. Includes data loading, basic preprocessing, model training, and evaluation. Designed as a foundational exercise in supervised learning.


## What's Inside

- `data/`: folder for dataset files. Raw CSV is not included in the repo due to size limits; download link is provided below.
- `notebooks/`: contains the main analysis notebook (`main_analysis.ipynb`) with the complete ML workflow.
- `requirements.txt`: Python dependencies for local environment.
- `LICENSE` and `.gitignore`: standard repository configuration.


## Dataset

The dataset contains passengers' responses to a post-flight surve, including satisfaction labels.  
**Download source:** https://edu.sirius.online/noo-back/files/3bad0257e41f6fc9d9fa4900dcdb89b1115dec71.csv
**Size:** 129880 rows, M features.  

After downloading, place the CSV file in the `data/` folder.


## Running the Project
For Google Colab: Run the first cell of the notebook to install dependencies.
For local environment: pip install -r requirements.txt

1. Clone the repository:
   git clone https://github.com/Ksenia-Krv/sirius-ml-intro-project-1.git
2. Navigate to the project folder:
cd sirius-ml-intro-project-1
3. Install dependencies:
pip install -r requirements.txt
4. Launch Jupyter Notebook:
jupyter notebook
5. Open notebooks/main_analysis.ipynb and run all cells.


## Approach and Key Steps

The notebook follows a standard supervised learning pipeline:
- **Data loading**: the CSV is loaded with `pandas`, basic shape and column types are inspected (`df.shape`, `df.info()`).
- **Exploratory Data Analysis (EDA)**: basic statistics (`df.describe()`) and simple visualizations (distribution of the target, correlations) are used to understand the data structure.
- **Preprocessing**:
  - Handling missing values
  - Encoding categorical features
  - Scaling numeric features.
- **Train/test split**: data is split into training and test sets using `train_test_split` with a fixed `random_state=100` to ensure reproducibility.
- **Model training**: a baseline classifier (**LogisticRegression**) is trained on the training set.
- **Evaluation**: model performance is assessed on the test set using **accuracy**, **precision**, **recall**, and **F1-score**; a confusion matrix is plotted for visual interpretation.


## Results

The baseline model (**LogisticRegression**) achieved the following performance on the held-out test set:

- **Accuracy**: **[ВСТАВЬ ЗНАЧЕНИЕ, НАПРИМЕР: 0.78]**
- **Precision**: **[ВСТАВЬ ЗНАЧЕНИЕ ИЛИ НАПИШИ: see notebook]**
- **Recall**: **[ВСТАВЬ ЗНАЧЕНИЕ ИЛИ НАПИШИ: see notebook]**
- **F1-score**: **[ВСТАВЬ ЗНАЧЕНИЕ ИЛИ НАПИШИ: see notebook]**

> Note: These metrics are based on a single train/test split with `random_state=100`. For more robust estimates, cross-validation can be added in future iterations.


## How to Reproduce the Results

To get exactly the same numbers:

1. Ensure `random_state=100` is used in `train_test_split` and in the model constructor (if supported).
2. Run all notebook cells.
3. Use the exact same preprocessing steps as implemented in the notebook.
4. Evaluate on the same test split without additional shuffling.


## Author
**Ksenia-Krv**


## License
This project is licensed under the MIT License — see the `LICENSE` file for details.
