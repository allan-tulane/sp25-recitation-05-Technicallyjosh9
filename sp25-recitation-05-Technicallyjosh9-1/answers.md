# CMPS 2200 Reciation 5
## Answers

**Name:** Joshua Haddad


Place all written answers from `recitation-05.md` here for easier grading.





- **1b.**
Random Shuffle

|      n |   qsort-fixed-pivot |   qsort-random-pivot | 
|--------|---------------------|----------------------|
|    100 |               0.250 |                0.231 | 
|    200 |               0.451 |                0.369 |   
|    500 |               1.048 |                1.075 |      
|   1000 |               2.280 |                1.795 |    
|   2000 |               5.009 |                4.664 |     
|   5000 |              11.616 |               10.498 |     
|  10000 |              20.445 |               20.465 |     
|  20000 |              44.496 |               45.778 |   
|  50000 |             166.391 |              124.618 |  
| 100000 |             288.874 |              295.284 |   
Theoretical asymptotes
qsort-fixed-pivot: O(nlog(n))
qsort-random-pivot:O(nlog(n))

These results match the theoretically determined asymptotes because at the largest list size of 100000 the two runtimes of the algorithms are nearly identical.

Not Shuffled
|      n |   qsort-fixed-pivot |   qsort-random-pivot | 
|--------|---------------------|----------------------|
|    100 |               0.117 |                0.107 |   
|    200 |               0.300 |                0.276 |     
|    500 |               0.767 |                0.728 |    
|   1000 |               1.642 |                1.746 |    
|   2000 |               4.093 |                3.472 |    
|   5000 |               7.788 |                7.899 |    
|  10000 |              22.399 |               15.804 |     
|  20000 |              37.181 |               34.898 |     
|  50000 |             102.700 |              105.673 |   
| 100000 |             214.021 |              198.894 |    

Theoretical asymptotesqsort-fixed-pivot: O(n^2)
qsort-random-pivot:O(nlog(n))

These results match the theoretically determined asymptotes because at the largest list size of 100000 the qsort-fixed-pivot runtime is larger than the qsort-random-pivot which makes sense becayse O(n^2) is greater than O(nlog(n)).

Changing the input from ordered to disordered results in an increase in time for qsort-fixed-pivot because it is the worst-case scenario for this algorithm, while changing the input for qsort-random-pivot does not affect runtime at all because the algorithm reshuffles its pivot every step of the way, so its runtime is going to be consistent no matter the type of order.

- **1c.**
Random Shuffle

|      n |   qsort-fixed-pivot |   qsort-random-pivot |   tim_sort |
|--------|---------------------|----------------------|------------|
|    100 |               0.250 |                0.231 |      0.010 |
|    200 |               0.451 |                0.369 |      0.018 |
|    500 |               1.048 |                1.075 |      0.047 |
|   1000 |               2.280 |                1.795 |      0.090 |
|   2000 |               5.009 |                4.664 |      0.326 |
|   5000 |              11.616 |               10.498 |      0.480 |
|  10000 |              20.445 |               20.465 |      1.247 |
|  20000 |              44.496 |               45.778 |      3.173 |
|  50000 |             166.391 |              124.618 |      7.149 |
| 100000 |             288.874 |              295.284 |     17.241 |

Theoretical asymptotes
qsort-fixed-pivot: O(nlog(n))
qsort-random-pivot:O(nlog(n))times_sort:O(nlog(n))

These results match the theoretically determined asymptotes because at the largest list size of 100000 the qsort-fixed-pivot runtime is larger than the qsort-random-pivot which makes sense becayse O(n^2) is greater than O(nlog(n)).

Not Shuffled
|      n |   qsort-fixed-pivot |   qsort-random-pivot |   tim_sort |
|--------|---------------------|----------------------|------------|
|    100 |               0.117 |                0.107 |      0.002 |
|    200 |               0.300 |                0.276 |      0.003 |
|    500 |               0.767 |                0.728 |      0.004 |
|   1000 |               1.642 |                1.746 |      0.012 |
|   2000 |               4.093 |                3.472 |      0.015 |
|   5000 |               7.788 |                7.899 |      0.030 |
|  10000 |              22.399 |               15.804 |      0.070 |
|  20000 |              37.181 |               34.898 |      0.257 |
|  50000 |             102.700 |              105.673 |      0.310 |
| 100000 |             214.021 |              198.894 |      0.746 |

Theoretical asymptotesqsort-fixed-pivot: O(n^2)
qsort-random-pivot:O(nlog(n))
timss_sort:O(n)

These results match the theoretically determined asymptotes because at the largest list size of 100000 the tim_sort shuffled runtime is larger than the tim_sort not shuffled runtime which makes sense becayse O(nlog(n)) is greater than O(n). This is the case because tim_sorts best case scenario is that the list is already sorted and in an other case it runs in O(nlog(n)) time which is supported by our data.