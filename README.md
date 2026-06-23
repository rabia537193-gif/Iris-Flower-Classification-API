Iris Flower Classification APIAn end-to-end Machine Learning web service that trains a Random Forest Classifier on the Iris dataset and exposes it via a high-performance FastAPI application.  🛠️ Project StructureIris_Flower_Classification_API.ipynb — Full notebook for training, API building, and deployment.  app.py — The production-ready FastAPI application script.  iris_model.pkl — The saved/serialized machine learning model file.  🚀 Setup & Execution1. Install DependenciesBashpip install fastapi uvicorn joblib scikit-learn pyngrok
2. Run the API LocallyBashuvicorn app:app --reload
Local Docs: Open [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) for the interactive Swagger UI.🔌 API Endpoints🟢 GET /Returns a simple welcome message.  🔵 POST /predictClassifies an Iris flower species based on its measurements.  Request Body:JSON{
  "sepal_length": 5.1,
  "sepal_width": 3.5,
  "petal_length": 1.4,
  "petal_width": 0.2
}
Response:JSON{
  "prediction": "setosa"
}
🌐 Public Testing via NgrokIf running inside Google Colab, you can easily expose this local API to the public internet using the integrated pyngrok configuration block inside the Iris_Flower_Classification_API.ipynb notebook.  
