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
G=1000;
lambda = 0.03;
sigma = 1;
Pmin = 1e-10;
Pt = 1:100:10000;
Rmax1= ((Pt.*(G^2).*(lambda^2).*sigma)./(((4*%pi)^3)*Pmin)).^(1/4);
Pmin2 = 1e-12:1e-12:1e-9;
Pt_const = 5000;
Rmax2 = ((Pt_const*(G^2)*(lambda^2)*sigma)./ (((4*%pi)^3)*Pmin2)).^(1/4);
subplot(2,1,1)
plot(Pt,Rmax1)
subplot(2,1,2)
plot(Pmin2,Rmax2)
```

### Tabulation

![WhatsApp Image 2026-04-08 at 21 02 13](https://github.com/user-attachments/assets/76e02568-11ad-45b5-ae19-2b4eda975913)

### Output

<img width="1918" height="1130" alt="image" src="https://github.com/user-attachments/assets/3d761db3-4180-423f-934a-7f4c6f4333c5" />


### Result

Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
