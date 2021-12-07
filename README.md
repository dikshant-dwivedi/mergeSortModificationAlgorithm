# Merge Sort Algorithm Modification

## Attempt 1: Where we started? Motivation

* Started with the idea that
* Insertion sort works better with smaller arrays
* Merge sort is an efficient sorting algorithm that divides array into smaller sub arrays
* To improve running time of the merge sort algorithm, we decided to combine merge and insertion sort.

## Attemp 1: What we did

* In the merge sort algorithm, an array is divided into two halves and keeps dividing into smaller and smaller parts until the size of subarrays become trivial (one).
* The two things that we decided to modify upon were:
* What if, instead of two halves, we always divide the array into n halves
* What if, the smallest size of subarray is more than one
* What if, for these smaller subarrays, insertion sort is used instead
* So, for the following algorithm we tried to observe and compare merge sort running time with an algorithm where the following tweaks were made
* by dividing the array into 2, 3, 4, 5 and 6 halves
* with insertion sort conducted on smallest subarrays with various sizes

<p align = "center">
  <img src="/readMeAssets/attemptOne.PNG" width = "80%"/>
</p>

<p align = "center">
  <img src="/readMeAssets/observationOne.PNG" width = "80%"/>
</p>

## Attempt 1: Conclusion
Looking at the previous table, it can be deduced that there were no significant differences in the running time between the original merge sort and tweaked version. We have tried to summarize the observations as follows:

<p align = "center">
  <img src="/readMeAssets/conclusionOne.PNG" width = "80%"/>
</p>

## Attempt 2: Replacing min max sort with insertion sort

* After observing very little changes by using merge sort with insertion sort, we decided replace insertion sort with min-max selection sort.
* Min-max selection sort improves upon the execution time of selection significantly since:
* Selection sort algorithm takes the minimum on every pass on the array and place it at its correct position.
* Min-max selection sort takes both minimum and maximum on single pass and place them at their correct position, in this way the array gets sorted in half the iterations.
* Min-max selection sort is not much faster than insertion sort but we expect faster result in min max sort for moderate sized arrays.

<p align = "center">
  <img src="/readMeAssets/timeComparison.PNG" width = "80%"/>
</p>

## Attempt 2: What we did

* In the merge sort algorithm, an array is divided into two halves and keeps dividing into smaller and smaller parts until the size of subarrays become trivial (one).
* The two things that we decided to modify upon were:
  * What if, instead of two halves, we always divide the array into n halves
  * What if, the smallest size of subarray is more than one
  * What if, for these smaller subarrays, min-max selection sort is used instead
* So, for the following algorithm we tried to observe and compare merge sort running time with an algorithm where the following tweaks were made
  * by dividing the array into 2, 3, 4, 5 and 6 halves
  * with min-max selection conducted on smallest subarrays with various sizes
  
<p align = "center">
  <img src="/readMeAssets/attemptTwo.PNG" width = "80%"/>
</p>

<p align = "center">
  <img src="/readMeAssets/observationTwo.PNG" width = "80%"/>
</p>

## Attempt 2: Conclusion
General trends of our original table remain unchanged from attempt 1 conclusions, that is increasing the halves in merge sort increase running time and using min-max i for smaller subarrays reduce recursion call and increase running time by 10-15%. However, in some aspects, min-max sort perform much better than insertion sort in our tweaked algorithm. They are summarized here:

<p align = "center">
  <img src="/readMeAssets/conclusionTwo.PNG" width = "80%"/>
</p>

## Source Code link
<a href="https://colab.research.google.com/drive/123mIVIdBTA8DIu3Tdf72xvWfg8Xjprx4?usp=sharing" target="_blank">https://colab.research.google.com/drive/123mIVIdBTA8DIu3Tdf72xvWfg8Xjprx4?usp=sharing</a>

