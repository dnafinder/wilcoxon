# wilcoxon
Non parametric Wilcoxon test to evaluate the difference between paired (dependent) samples. <br/>
If the number of difference is less than 15, the algorithm calculate the exact ranks distribution; 
else it uses a normal distribution approximation. 
Now, the MatLab function SIGNRANK returns the same p-value. 
Anyway, this Wilcoxon function gives a more detailed output (that is necessary for publications...)

Syntax: 	STATS=WILCOXON(X1,X2,PLTS)
     
    Inputs:
          X1 and X2 - data vectors.
          ALPHA - significance level (default = 0.05).
          PLTS - Flag to set if you don't want (0) or want (1) view the plots
    Outputs:
          - W value and p-value when exact ranks distribution is used.
          - W value, Z value, Standard deviation (Mean=0), p-value when normal distribution is used
       If STATS nargout was specified the results will be stored in the STATS
       struct.

     Example: 

        X1=[77 79 79 80 80 81 81 81 81 82 82 82 82 83 83 84 84 84 84 85 85 86 86 87 87];

        X2=[82 82 83 84 84 85 85 86 86 86 86 86 86 86 86 86 87 87 87 88 88 88 89 90 90];

          Calling on Matlab the function: wilcoxon(X1,X2)

          Answer is:

WILCOXON TEST
 
                                Mean_of_differences    Confidence_interval
                                ___________________    ___________________

    Binomial_estimator            3                    3    4             
    Hodges_Lehmann_estimator    3.5                    3    4             

Sample size is good enough to use the normal distribution approximation
 
     W     Mean      SD        Z       p_value_two_tails
    ___    ____    ______    ______    _________________

    325    0       73.161    4.4354    9.1886e-06       

          Created by Giuseppe Cardillo
          giuseppe.cardillo-edta@poste.it

To cite this file, this would be an appropriate format:
Cardillo G. (2006). Wilcoxon test: non parametric Wilcoxon test for paired samples.
http://www.mathworks.com/matlabcentral/fileexchange/12702
