# Detection of anomalies using the Scan Statistic and Local Score methods
## Abstract
Mathematical researchers are regularly looking for new scan methods to detect atypical segments in datasets. Scan methods have wide applications in medicine or actuary science. Previous work has tried to find methods to reveal irregularities within a discrete sequence of events using the local score method, defined by the log-likelihood ratio. However, these methods have not proposed a time-continuous scan on an interval from $0$ to $T$. We propose a new method using scan statistic and Local Score to apply on continuous data and to detect atypical segments. We compare the performance of both algorithms. We simulate three sets of $10^4$ Poisson processes of a certain parameter $\lambda$. We use one set to estimate the empirical distribution of the scan statistic, using a Monte Carlo estimator. On the same set, we compute the sequence of times between events to estimate the score distribution. With the two other sets, we associate to each scan or score value, its p-value, that states if the detected segment is atypical. We conduct this experiment, knowing the value of the scan window, and then by choosing it at random.  Results show that both methods have a good prediction quality. The Scan statistic method performs more accurately when knowing the window-size. Local Score outperforms the Scan statistic method when using random values for the window size. Applications on real datasets, such as epileptic seizures, are an opening for the use of these methods.


**Keywords:**  scan statistic, Poisson process, local score, detection of atypical regions, window size

## Code R on the comparison of methods
In this project, we have tried to implement a new method of scan statistic, using both the Local Score and the scan statistic method. In order to do so, the code [Comparaison_of_methods](./Comparaison_of_methods.rmd) explains step by step the process of creating the sequences, estimating the empirical scan distribution and the empirical score distribution and the computation of the p-values. 
The comparison of the method has been made on the study of performance curves and confusion matrix, for several values for $(\lambda_0,\lambda_1)$, $\tau$, $\tau_o$ and $\alpha$. Further details are given on the paper. 

## Dependencies
### R libraries
To run and compile the code [Comparaison_of_methods](./Comparaison_of_methods.rmd) in PDF format, please use the following command in R terminal before running the file:
```
install.packages(c("localScore", "latex2exp", "Rcpp", "caret", "ROCR", "pROC"))
```
