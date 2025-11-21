# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


## ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation
   
## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results

## PROGRAM:
```
clear; clc; clear;

function X = f(x)
    z = 3 * (1 - x)^2;
    X = x * z;
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);

function Y = c(y)
    z = 3 * (1 - y)^2;
    Y = y * z;
endfunction

EY = intg(a, b, c);

disp(EX, "i)Mean of X =");
disp(EY, "Mean of Y =");

function X = g(x)
    z = 3 * (1 - x)^2;
    X = x^2 * z;
endfunction

EX2 = intg(a, b, g);

function Y = h(y)
    z = 3 * (1 - y)^2;
    Y = y^2 * z;
endfunction

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp(vX2, "ii)Variance of X");
disp(vY2, "Variance of Y");

x = input("type in the reference sequence=");
y = input("type in the second sequence=");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
plot2d3('gnn', r);
```

## CALCULATION:
![515757402-451f5bc8-b88b-4c49-bf21-f0089e6fb937](https://github.com/user-attachments/assets/2399fa1d-44b2-40f6-8cd0-33b127d88336)
![515757483-1d71678a-a7c1-4c78-b273-e6b603a8e86f](https://github.com/user-attachments/assets/7f17b6a8-ea87-488a-a371-41a54386a96e)

## OUTPUT:
<img width="660" height="542" alt="515757571-df1fcf8f-b1f2-4bfc-9349-a3bb549ed2a5" src="https://github.com/user-attachments/assets/d537a863-8809-425b-a436-0b3b3fa6887d" />

## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.

