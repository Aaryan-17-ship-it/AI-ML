# AI-ML
House Price Predictor Project
<br>
Author: Aaryan Jha
<br>
Project Title: House Price Predictor
<br>
<br>
❖ Overview of the Project:
<br>
<br>
This application predicts property values based on square footage and the number of rooms. It uses a Linear Regression model trained on market standards to provide an estimated price when an exact match for the user's criteria is not found in the existing dataset.
<br>
<br>
❖ Features:
<br>
➤ Exact Match Search: Checks if the specific square footage and room count exist in the current database.
<br>
➤ AI Prediction: Utilizes Scikit-Learn to predict prices for properties that fall outside the immediate dataset.
<br>
➤ Data Visualization: Generates a scatter plot using Matplotlib to show how the user's selection compares to market trends.
<br>
➤ Error Handling: Validates user input to ensure only numeric values are processed.
➤ Error Handling: Validates user input to ensure only numeric values are processed.
<br>
<br>
❖ Technologies/Tools Used:
<br>
1. Programming Language
Python 3.x Used to implement the logic, handle user inputs, and manage data structures.
<br>
<br>
2. Libraries
<br>
Pandas: Used for data manipulation and creating the DataFrame.
<br>
Matplotlib: Used for rendering the visual trend graphs.
<br>
Scikit-Learn: Used to implement the LinearRegression model for AI-based price estimation.
<br>
<br>
3. Runtime Environment
<br>
Python Interpreter Executes the .py file and displays both the terminal interface and the graphical output.
<br>
<br>
❖ Steps to Install & Run the Project:
<br>
❖ Instructions for Testing:
<br>
<br>
➤ Open VS Code with the Python extension installed.
<br>
➤ Ensure you have the required libraries installed by running:
<br>
➤ pip install pandas matplotlib scikit-learn
<br>
➤ Save the project file (e.g., house_price_predictor.py) on your computer.
<br>
➤ To verify your installation, run:
<br>
➤ python --version
<br>
➤ How to Run the Program
<br>
➤ Open Command Prompt / Terminal.
<br>
➤ Navigate to the folder where the file is saved:
<br>
➤ cd path/to/your/project
<br>
➤ Run the application:
<br>
➤ python house_price_predictor.py
<br>
<br>
<br>
❖ Expected Program Flow:
<br>
➤ System initializes the dataset and trains the Linear Regression model.
<br>
➤ User enters the Square Footage.
<br>
➤ User enters the Number of Rooms.
<br>
<br>
<br>
❖ Program displays:
<br>
➤ The exact price if a match is found.
<br>
➤  An "AI Estimated Market Price" if no exact match exists.
<br>
➤ A window opens showing a graph of Price vs. Square Footage with the user's selection highlighted.
