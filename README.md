# 🧠 Stroke Prediction using Machine Learning Pipeline

This project uses a Decision Tree Classifier to predict the likelihood of a stroke based on medical and demographic features. The model is built using a complete preprocessing and modeling pipeline in scikit-learn, including imputation, encoding, feature selection, and classification.

---

## 📂 Project Structure

├── StrokePrediction_WithPipelines.ipynb          # Main ML pipeline notebook
├── Prediction_Using_Pipeline.ipynb               # Prediction logic using trained pipeline
├── healthcare-dataset-stroke-data.csv            # Dataset (from Kaggle)
├── pipe.pkl                                      # Saved model pipeline 
├── requirements.txt                              # List of Python packages required
└── README.md                                     # Project documentation


---

## 📊 Dataset

- **Source:** [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset)
- **Features:**
  - `gender`, `age`, `hypertension`, `heart_disease`, `ever_married`, `work_type`, `Residence_type`, `avg_glucose_level`, `bmi`, `smoking_status`
- **Target:**
  - `stroke` (1: patient had a stroke, 0: did not)

---

## 🛠️ Preprocessing Steps

- **Imputation:** Missing values in `bmi` handled using `SimpleImputer (median)`
- **Encoding:**
  - `OneHotEncoder`: for categorical features like gender, work_type, smoking_status
  - `OrdinalEncoder`: for binary features like ever_married, Residence_type
- **Feature Selection:** `SelectKBest` using Chi-squared test
- **Model:** `DecisionTreeClassifier`
- **Pipeline:** Entire workflow wrapped using `ColumnTransformer` and `Pipeline` from scikit-learn

---

## 🚀 How to Run

1. **Clone the repository**  
```bash
   git clone https://github.com/Anshika17S/Stroke_Prediction_Model.git
   cd Stroke_Prediction_Model
   ```

2. **Install dependencies**
    (Make sure Python is installed, and use a virtual environment if needed)
```bash
pip install -r requirements.txt
```

3. **Run the notebooks**

- 📘 `StrokePrediction_WithPipelines.ipynb`  
  This is the main notebook where the pipeline is built, trained, and evaluated using the dataset.

- 🔍 `Prediction_Using_Pipeline.ipynb`  
  This notebook loads the saved pipeline (`pipe.pkl`) using `pickle` and makes predictions on new data.

  > ⚙️ This project requires **Python 3.8+** and works well with **Jupyter Notebook** or **VS Code** (with Jupyter extension).


  ## 👩‍💻 Author

**Anshika Sharma**

- [GitHub](https://github.com/Anshika17S)
- [LinkedIn](https://www.linkedin.com/in/anshika-sharma-135a47316/)
- [Kaggle](https://www.kaggle.com/anshika17s)

## 📝 License

This project is licensed under the [MIT License](LICENSE).
