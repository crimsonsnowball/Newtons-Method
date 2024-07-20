This project focuses on fitting a sinusoid to a set of given measurements taken over time. Specifically, we have 𝑚
m measurements of a process at m points in time. The measurement times are denoted by t1, t2, ..., tm, and the corresponding measurement values are y1, y2, ..., ym. In the example depicted in Figure 9.2, we have 21 measurements where t1 equals 0 and t21 equals 10.
The sinusoidal function we aim to fit to the data is given by:
y = A * sin(ω * t + φ)
where A is the amplitude, ω is the angular frequency, and φ is the phase shift.
To find the best fit, we construct the objective function that represents the sum of the squared errors between the measured values and the values predicted by our sinusoidal model:
sum((yi - A * sin(ω * ti + φ))^2 for i in 1 to m)
We represent the parameters we need to determine (amplitude A, angular frequency ω, and phase shift φ) as the vector x = [A, ω, φ].
This formulation results in a nonlinear least-squares problem, where our goal is to minimize the objective function to find the best-fitting parameters. The residuals ri(x) are given by:
ri(x) = yi - A * sin(ω * ti + φ)
