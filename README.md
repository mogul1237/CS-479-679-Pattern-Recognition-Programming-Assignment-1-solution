# CS-479-679-Pattern-Recognition-Programming-Assignment-1-solution

Download Here: [CS 479/679 Pattern Recognition Programming Assignment 1 solution](https://jarviscodinghub.com/assignment/cs-479-679-pattern-recognition-programming-assignment-1-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Let us assume a two-class classification problem where each class is modeled by a 2D
Gaussian distribution G(μ1, Σ1) and G(μ2, Σ2).
1. Generate 100,000 samples from each 2D Gaussian distribution (i.e., 200,000 samples
total) using the following parameters (i.e., each sample (x,y) can be thought as a feature
vector):
1
1
1

 
    
1
1 0
0 1
       

2
4
4

 
    

2
1 0
0 1
       
Notation:
x
y



 
    

2
2
0
0
x
y


 
       

Note: this is not the same as sampling the 2D Gaussian functions; see “Generating
Gaussian Random Numbers“on the course’s webpage for more information on how to
generate the samples using the Box-Muller transformation. A link to C code has been
provided on the webpage. Since the code generates samples for 1D distributions, you
would need to call the function twice to get a 2D sample (x, y); use (μx, σx) for the x
sample and (μy, σy) for the y sample.
Note: ranf() is not defined in the standard library and that you would need to
implement it yourself using rand(); for example:
/* ranf – return a random double in the [0,m] range.*/
double ranf(double m) {
return (m*rand())/(double)RAND_MAX;
}
(m=1 in our case)
a. Assuming P(ω1) = P(ω2)
i. Design a Bayes classifier for minimum error.
ii. Plot the Bayes decision boundary together with the generated samples
to better visualize and interpret the classification results.
iii. Report (i) the number of misclassified samples for each class separately
and (ii) the total number of misclassified samples.
iv. Plot the Chernoff bound as a function of β and find the optimum β for the
minimum.
v. Calculate the Bhattacharyya bound. Is it close to the experimental error?
b. Repeat part (a) for P(ω1) = 0.2 and P(ω2) = 0.8. For comparison purposes, use
exactly the same 200,000 samples from (a) in these experiments.
2. Repeat parts (1.a) and (1.b) using the following parameters (i.e., you need to generate
new sample sets):
1
1
1

 
    

1
1 0
0 1
       

2
4
4

 
     2
4 0
0 8
       
3. Repeat part (2.b) (i.e., P(ω1) ≠ P(ω2)) using the minimum-distance classifier and
compare your results (i.e., misclassified samples) with those obtained in part (2.b). For
comparison purposes, use exactly the same 200,000 samples as in part 2.
