# Detection of anomalies using the Scan Statistic and Local Score methods
## Abstract
Mathematical researchers are regularly looking for new scan methods to detect anomalies in datasets. Scan methods have wide applications in medicine, actuary science or finance. Previous work has tried to find methods to reveal irregularities within a discrete sequence of events using the local score method, defined by the log-likelihood ratio. However, these methods have not proposed a time-continuous scan on an interval of $0$ to $T$. We propose a new method of scan statistic and the Local Score to apply on continuous data and to detect anomalies more accurately. We compare the performance of both algorithms. By simulating multiple samples of Poisson processes, we compute the scan statistic on a window of a given size that represents the maximal number of occurrences of an event. Then, we compute the time between events on these sequences, compute the local score and compare the two results, in terms of significance of occurrences. Results show that both methods have a good prediction quality. The Scan statistic method performs more accurately when knowing the window-size. Local Score outperforms the Scan statistic method when using random values for the window size. Applications on real datasets, such as epileptic seizures are an opening for the use of these methods.

**Keywords:**  scan statistic, Poisson process, local score, log-likelihood ratio, detection of atypical regions, window size


## Dependencies
### R libraries
To run and compile the code [Comparaison_of_methods](./Comparaison_of_methods.rmd) in PDF format, please use the following command in R terminal before running the file:
```
install.packages(c("localScore", "latex2exp", "Rcpp", "caret", "ROCR", "pROC"))
```
