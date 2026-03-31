# Battery Life Prediction for Mobile Devices Using Numerical Approximation

**Course:** MAT 403 - Numerical Analysis  
**Institution:** Bulacan State University, College of Science  
**Program:** BS in Mathematics with Specialization in Computer Science (BSM CS 4B)  

### Authors
* Francis Miguel G. Cabrera
* Richie Mae V. De Guzman
* Justine Bryan E. Espina
* Amaru Vjounce S. Pascual

---

## Project Overview
Battery life is a critical factor affecting the usability of mobile devices. However, predicting battery drain is difficult due to the highly non-linear nature of human usage (e.g., varying screen time, background apps, and charging habits). 

This project utilizes a **Hybrid Numerical Prediction Algorithm** to accurately model and estimate remaining battery life based on real-world survey data from 35 university students. By transitioning from traditional rigid formulas to dynamic numerical approximations, the model successfully predicted end-of-day battery levels with a Mean Absolute Error (MAE) of just **10.40%**.

## Mathematical Methods Utilized
This simulation integrates four key numerical techniques to create a continuous predictive framework from discrete data:
1. **Multiple Linear Regression (Robust Fit):** Used to establish a baseline discharge rate based on user-specific survey data. We also introduced a custom "Battery Wear Factor" (Device Age × Charging Frequency) to account for physical battery degradation.
2. **Finite Difference Approximation:** Used to estimate the continuous rate of change of the State of Charge (SoC).
3. **Euler's Method:** Discretizes the continuous differential equation to simulate battery drain step-by-step using a time step of `h = 0.5` hours (30 minutes).
4. **Linear Interpolation:** Allows the model to estimate battery percentages at specific times that do not fall perfectly on the discrete grid (e.g., estimating SoC at exactly 6.5 hours).

---

## Repository Contents
* `Battery_Prediction_Model.m` - The main MATLAB script containing the hybrid algorithm, simulation loop, and plotting functions.
* `Survey (Responses) (1).xlsx` - The raw dataset containing the physical and behavioral parameters of the 35 surveyed users.
* `BatterySimulation.png` - A high-quality export of the MATLAB computational graph demonstrating the Euler's Method steps for select users.
* `Final_Paper.pdf` - The complete expository research paper detailing the methodology, error analysis, and conclusions.

---

## How to Run the Code
To replicate the simulation and view the results:
1. Ensure you have **MATLAB** installed (or use MATLAB Online).
2. Download or clone this repository to your local machine.
3. **Important:** Ensure that the dataset (`Survey (Responses) (1).xlsx`) is located in the *same folder* as the MATLAB script.
4. Open the script in MATLAB and click **Run**.
5. The program will output a complete 10-column data table in the Command Window, displaying the discrete steps (6h, 7h, 8h), the interpolated step (6.5h), and the final error margins.
6. A Figure window will automatically open displaying the visual discharge curves.

---

## 📊 Results Summary
The computational simulation proves that numerical approximation is a highly effective tool for real-world engineering problems. By accounting for physical degradation and utilizing step-by-step Euler simulations, the model adapts to the unpredictability of human behavior, bridging the gap between abstract mathematical theory and everyday technology usage.
