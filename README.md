[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=13107769&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

1.
    1. Constants and lower order terms are ignored. Two algorithms with the same asymptotic complexity can run at different times because of them. 
    2. Differences in the hardware it's ran on.
    3. Asymptotic complexities can run faster if they pass a certain number of elements, and can run slower if less than that.

2.
    Finding how long the same element could be found with 10,000 elements could be done with the equation Runtime(m) / T(m) = Runtime(n) / T(n) where m and n are different sizes. This equation can give a good guess          because     the ratio of the runtime to the time complexity should be the same for any input size and given that the runtime of 1,000 elements is known, the numbers can be plugged in and the equation can be solved       to find the          runtime of different size data sets. Plugging in the numbers results in Runtime(10,000) / T(10,000) = Runtime(1,000) / T(1,000)
    Runtime(10,000) = T(10,000) * (5 / log(1,000))
    Runtime(10,000) = log(10,000) * (5 / log(1,000))
    Assuming log is base 2,
    Runtime(10,000) = 13.29 * 0.50 
    Runtime(10,000) = 6.6 secs

3.
    1. The computer it ran on could be running other programs in the background, causing slowdown when the algorithm is ran.
    2. A different machine was used to run the algorithm than what was used with 1,000 elements.
    3. Memory leaks.
