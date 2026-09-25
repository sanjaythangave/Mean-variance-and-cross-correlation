# Mean-variance-and-cross-correlation

# AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

# EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


# ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation

# PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results

# TABULATION

<img width="652" height="1310" alt="image" src="https://github.com/user-attachments/assets/c71e7bbf-8c8b-46be-ac1b-6af74bf595b9" />


# PROGRAM

clear;
clc;

// Mean of X
function X = f(x)
    z = 4 * (1 - x)^2;
    X = x * z;
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);

// Mean of Y
function Y = c(y)
    z = 4 * (1 - y)^2;
    Y = y * z;
endfunction

EY = intg(a, b, c);

disp(EX, "i) Mean of X =");
disp(EY, "i) Mean of Y =");

// Variance of X
function X = g(x)
    z = 4 * (1 - x)^2;
    X = x^2 * z;
endfunction

EX2 = intg(a, b, g);

// Variance of Y
function Y = h(y)
    z = 4 * (1 - y)^2;
    Y = y^2 * z;
endfunction

EY2 = intg(a, b, h);

vX = EX2 - EX^2;
vY = EY2 - EY^2;

disp(vX, "ii) Variance of X =");
disp(vY, "ii) Variance of Y =");

// Cross Correlation
x = input("Type in the reference sequence: ");
y = input("Type in the second sequence: ");

n1 = length(y) - 1;
n2 = length(x) - 1;

// Cross-correlation
r = corr(x, y, n1);

disp(r, "Cross Correlation =");

// Plot
plot2d3(r);
xtitle("Cross Correlation", "Lag", "Correlation");




# OUTPUT
i)	Mean of X =	0.333 Mean of Y =	0.333

ii)	Variance of X	 0.0222 Variance of Y	0.0222

Cross Correlation
Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]
 

# RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
