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
Battery Life has become a significant design parameter in mobile systems as energy capacity of batteries is one of the key factors that determine usability of mobile devices. However, accurately predicting battery life for a given workload is a difficult task due to the inherently non-linear behavior of real-world power consumption resulting from real-world human interactions.

This project used a **Hybrid Numerical Prediction Algorithm** to predict remaining battery life by using real-world data collected from a survey of 35 students from a university. Using a hybrid numerical approximation instead of a rigid equation allowed for accurate prediction of the end-of-day battery level with an average error of **10.40%**.

## Mathematical Methods Utilized
This simulation integrates four key numerical techniques to create a continuous predictive framework from discrete data:
1. **Multiple Linear Regression:** Used to establish a baseline discharge rate based on user-specific survey data. We also introduced a custom "Battery Wear Factor" (Device Age × Charging Frequency) to account for physical battery degradation.
2. **Finite Difference Approximation:** Used to estimate the continuous rate of change of the State of Charge (SoC).
3. **Euler's Method:** Converts the continuous differential equation into discrete form to mimic battery depletion incrementally with a time increment of `h = 0.5` hours (30 minutes)
4. **Linear Interpolation:** Allows the model to estimate battery percentages at specific times that do not fall perfectly on the discrete grid (e.g., estimating SoC at exactly 6.5 hours).

---

## Repository Contents
* `Code.mlx` - The main MATLAB script containing the hybrid algorithm, simulation loop, and plotting functions.
* `Survey (Responses).xlsx` - The raw dataset containing the physical and behavioral parameters of the 35 surveyed users.
* `BatterySimulation.png` - A high-quality export of the MATLAB computational graph demonstrating the Euler's Method steps for select users.
* `NumAnalysis___Battery_Life_Prediction_for_Mobile_Devices_Using_Numerical_Approximation.pdf` - The complete expository research paper detailing the methodology, error analysis, and conclusions.

---

## How to Run the Code
To replicate the simulation and view the results:
1. Ensure you have **MATLAB** installed (or use MATLAB Online).
2. Download or clone this repository to your local machine.
3. **Important:** Ensure that the dataset (`Survey (Responses).xlsx`) is located in the *same folder* as the MATLAB script.
4. Open the script in MATLAB and click **Run**.
5. The program will output a complete 10-column data table in the Command Window, displaying the discrete steps (6h, 7h, 8h), the interpolated step (6.5h), and the final error margins.
6. A Figure window will automatically open displaying the visual discharge curves.

---

## Results Summary
The code simulation demonstrates that numerical approximation is an extremely efficient method for practical engineering challenges. The model accommodates physical deterioration and employs incremental Euler simulations to respond to the variability of human behavior, connecting abstract mathematical concepts with practical technology application
