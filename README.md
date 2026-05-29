# Web Application Integrated with Machine Learning

This project is a web application built with **Flask** and integrated with a Machine Learning model to estimate annual salaries based on user-provided information.

The application provides a simple web form where users can enter professional and demographic information, such as country, education level, developer role, and years of experience. After submission, the data is processed, scaled, and passed to a trained Machine Learning model to generate a salary prediction.

## Project Objective

The objective of this project is to demonstrate how to integrate a trained Machine Learning model into a web application, allowing users to interact with the model through a simple browser-based interface.

The project covers:

* Building a web application with Flask;
* Creating an HTML form for user input;
* Loading a trained Machine Learning model;
* Applying data preprocessing with a saved scaler;
* Returning salary predictions through a web interface;
* Running the application locally or with Gunicorn.

## Technologies Used

* Python
* Flask
* HTML
* CSS
* Scikit-learn
* Pickle
* Gunicorn
* Pandas
* NumPy

## Project Structure

```text
.
├── app.py              # Main Flask application
├── home.html           # Web page with the prediction form
├── styles.css          # CSS file for styling the web page
├── dsa_modelo.pkl      # Trained Machine Learning model
├── dsa_scaler.pkl      # Scaler used for preprocessing
├── requirements.txt    # Project dependencies
├── LEIAME.txt          # Original execution instructions
└── README.md           # Project documentation
```

## How the Project Works

The application follows this workflow:

1. The user accesses the home page;
2. The web form is displayed in the browser;
3. The user enters the required information:

   * Country;
   * Education level;
   * Developer role;
   * Years of experience;
4. The application validates the input fields;
5. The input data is transformed using a saved scaler;
6. The trained Machine Learning model generates the salary prediction;
7. The estimated annual salary is displayed on the web page.

## Input Features

The model uses the following input variables:

| Feature    | Description                      |
| ---------- | -------------------------------- |
| Country    | User's country                   |
| education  | User's education level           |
| devtype    | User's professional role         |
| experience | Years of professional experience |

## Installation

Create a Conda virtual environment:

```bash
conda create --name dsaengsoftp1 python=3.12
```

Activate the environment:

```bash
conda activate dsaengsoftp1
```

Install `pip` and the project dependencies:

```bash
conda install pip
pip install -r requirements.txt
```

## Running the Application

From the project folder, run the application using Gunicorn:

```bash
gunicorn -w 4 app:app
```

After running the command, open the application in your browser using the local address provided by the server.

## Web Interface

The application includes a simple web page where users can select or enter the required information and submit the form to receive a salary prediction.

The prediction result is displayed directly on the page as an estimated annual salary.

## Notes

* The trained model must be available as `dsa_modelo.pkl`.
* The scaler must be available as `dsa_scaler.pkl`.
* The application expects all form fields to be completed before making a prediction.
* This project was developed for educational purposes and demonstrates the integration of Machine Learning models into web applications.

## Author

Project developed as a practical study on building web applications integrated with Machine Learning models.
