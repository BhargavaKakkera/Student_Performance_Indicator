## 📊 Student Performance Predictor – ML Web App

This project predicts a student's **math score** based on their background and test performance. It's a full ML pipeline using **Flask**, **scikit-learn**, and **Docker**, with a user-friendly web interface.


### 🚀 Live Demo & Deployment

#### 🌐 Render Deployment (Recommended for Web Hosting)

🔗 **Live App on Render**: [https://student-performance.render.com](https://student-performance.render.com)

👉 Click above to try it live!

⚙️ **Deployment Instructions**:

1. Create a free account at [https://render.com](https://render.com)
2. Connect your GitHub repository.
3. Set build and start commands:

   * **Build Command**: `pip install -r requirements.txt`
   * **Start Command**: `python app.py`
4. Add `.render.yaml` for automated deployment.

```yaml
services:
  - type: web
    name: student-performance
    env: python
    buildCommand: "pip install -r requirements.txt"
    startCommand: "python app.py"
    plan: free
```

---

#### 🐳 Docker Deployment

🔗 **DockerHub Image**: [bhargava1420/student-performance](https://hub.docker.com/r/bhargava1420/student-performance)

```bash
docker pull bhargava1420/student-performance:latest
docker run -p 5000:5000 bhargava1420/student-performance
```

Visit [http://localhost:5000](http://localhost:5000) in your browser.

---

### 🧠 ML Model Info

* **Models Tried**: Linear Regression, Lasso, Ridge, Decision Tree, Random Forest, XGBoost, CatBoost, SVR, KNN
* **Final Model Used**: **Linear Regression**
* **Target Variable**: `Math Score`

**Features Used**:

* Gender
* Race/Ethnicity
* Parental Education
* Lunch Type
* Test Preparation Course
* Reading Score
* Writing Score

---

### 🖼️ App Screenshot

![App Screenshot](assets/screenshot.png)

---

### 📁 Folder Structure

```
student-performance-indicator/
├── app.py
├── Dockerfile
├── .render.yaml
├── requirements.txt
├── templates/
│   ├── index.html
│   └── home.html
├── src/
│   ├── notebook/
│   │   ├── eda.ipynb
│   │   └── model_trainer.ipynb
│   ├── pipeline/
│   │   └── predict_pipeline.py
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── logger.py
│   ├── exception.py
│   └── utils.py
├── artifacts/   ← Contains saved model.pkl, transformer.pkl
```

---

### 🦪 Run Locally Without Docker

```bash
# Step 1: Create virtual environment
python -m venv venv
venv\Scripts\activate  # On Windows
source venv/bin/activate  # On macOS/Linux

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Run the Flask app
python app.py
```

---

### ✅ Features

* Clean modular codebase with OOP principles
* Custom exception & logging handling
* Fully functional Flask web app for predictions
* Docker-ready & Render-ready deployment
* Model & preprocessor saved via Pickle

---

### 👤 Author

**Bhargava Kakkera**
📍 ECE Student at NIT Durgapur
🔗 GitHub: [BhargavaKakkera](https://github.com/BhargavaKakkera/Student_Performance_Indicator)
✉️ Email: [bhargavakakkera@gmail.com](mailto:bhargavakakkera@gmail.com)
