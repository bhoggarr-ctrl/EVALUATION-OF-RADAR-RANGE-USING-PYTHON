# EVALUATION-OF-RADAR-RANGE-USING-PYTHON

### Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.  

### Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by: 

<img width="257" height="328" alt="image" src="https://github.com/user-attachments/assets/c70a4df2-b0a2-4232-8e56-dec7942e9e58" />

### Procedure 
1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.  
2.	Import Necessary Libraries: Import the math library in Python.  
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.   
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.  
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.  
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.  


### Program
```
clc;
clear;
close;
Gt = 20;        
Gr = 30;        
lambda = 0.03;  
sigma = 1;      
Pmin = 1e-10;                 
Pt = linspace(1,1000,100);    
Rmax1 = ((Pt .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin)).^(1/4);
figure(1)
plot(Pt, Rmax1)
("Transmitted Power Pt")
("Maximum Range Rmax")
("Pt vs Rmax")
xgrid()
Pt_const = 500;                 
Pmin2 = linspace(1e-12,1e-8,100);
Rmax2 = ((Pt_const .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin2)).^(1/4);
figure(2)
plot(Pmin2, Rmax2)
("Minimum Detectable Power Pmin")
("Maximum Range Rmax")
("Pmin vs Rmax")
xgrid()

```

### Tabulation

<img width="542" height="738" alt="image" src="https://github.com/user-attachments/assets/c7f2e17a-db73-4c5a-92c5-26275e438424" />


### Output

<img width="1915" height="1198" alt="image" src="https://github.com/user-attachments/assets/1e9ef18b-6484-4d4e-84e4-a8c98baabd97" />
<img width="1916" height="1198" alt="image" src="https://github.com/user-attachments/assets/5dd9be79-813e-4436-b040-9d19dbad772d" />


### Result

Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.


