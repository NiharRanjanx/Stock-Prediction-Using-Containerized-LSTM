# Stock Prediction Using Containerized LSTM

## Overview
This project uses an LSTM (Long Short-Term Memory) model to predict stock prices based on historical data. It is packaged using Docker for portability, ensuring it runs seamlessly on any machine with Docker installed.

## Features
- Predicts stock prices using historical data and rolling averages.
- Uses an LSTM-based model for accurate forecasting.
- Containerized with Docker for easy deployment.

## Project Structure
```
stock-prediction-using-containerized-lstm/
|
├── app/
│   ├── app.py
│   ├── Dockerfile
│   ├── requirements.txt
│   ├── stacked_lstm_model.keras
│
├── model/
│   ├── stack_lstm_model_notebook.ipynb
│   ├── dataexploration.ipynb
│   ├── last_6_months_data.csv
│   ├── nse/
│       ├── dataset1.csv
│       ├── dataset2.csv
│       ├── ... (other datasets)
│
├── screenshots/ (optional for visuals)
│   ├── app_homepage.png
│   ├── prediction_results.png
│
└── README.md
```

## Technologies Used
- **Programming Language**: Python
- **Frameworks/Libraries**: Flask, TensorFlow, pandas, numpy, matplotlib
- **Tools**: Docker, Jupyter Notebook

## How to Run the Project

### Using Docker
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/stock-prediction-using-containerized-lstm.git
   ```
2. Navigate to the `app/` folder:
   ```bash
   cd stock-prediction-using-containerized-lstm/app
   ```
3. Build the Docker image:
   ```bash
   docker build -t stock-predictor .
   ```
4. Run the Docker container:
   ```bash
   docker run -p 5000:5000 stock-predictor
   ```
5. Open your browser and go to:
   ```
   http://localhost:5000
   ```

### Running Locally Without Docker
1. Navigate to the `app/` folder:
   ```bash
   cd stock-prediction-using-containerized-lstm/app
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask application:
   ```bash
   python app.py
   ```
4. Open your browser and go to:
   ```
   http://localhost:5000
   ```

## Model Training and Data Analysis
The `model/` folder contains:
- **Data Exploration**: Insights from the datasets using `dataexploration.ipynb`.
- **Model Training**: Training process in `stack_lstm_model_notebook.ipynb`.
- **Datasets**: Includes raw and processed data for training and testing.

## Screenshots (Optional)
![Homepage](screenshots/app_homepage.png)
*The homepage of the application.*

![Prediction Results](screenshots/prediction_results.png)
*Sample prediction results from the LSTM model.*

## Future Enhancements
- Add support for multiple stock indices.
- Deploy on cloud platforms like AWS or Render for broader accessibility.

## Contributing
Feel free to submit pull requests or raise issues to contribute to this project.

## License
This project is licensed under the [MIT License](LICENSE).
