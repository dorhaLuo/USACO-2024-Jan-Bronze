# Majority-Opinion-of-Cows
USACO 2024 January Contest, Bronze Problem 1. Majority Opinion


Problem: 
https://usaco.org/index.php?page=viewproblem2&cpid=1371

Farmer John has an important task - figuring out what type of hay to buy for his cows.

Farmer John's N cows (2≤N≤105) are numbered 1 through N and each cow likes exactly one type of hay h_i (1≤h_i≤N). He wants all his cows to like the same type of hay.

To make this happen, Farmer John can host focus groups. A focus group consists of getting all cows in a contiguous range numbered i to j, inclusive, together for a meeting. If there is a type of hay that more than half the cows in the group like, then after the focus group finishes meeting, all cows end up liking that type of hay. If no such type of hay exists, then no cows change the type of hay they like. For example, in focus group consisting of a range of 16 cows, 9 or more of them would need to have the same hay preference to cause the remaining cows to switch their preference to match.

Farmer John wants to know which types of hay can become liked by all cows simultaneously. He can only host one focus group at a time, but he can run as many focus groups as necessary to get all cows to like the same type of hay.

INPUT FORMAT (input arrives from the terminal / stdin):
The first will consist of an integer T, denoting the number of independent test cases (1≤T≤10).

The first line of each test case consists of N.

The second line consists of N integers, the favorite types of hay hi for the cows in order.

It is guaranteed that the sum of N over all test cases does not exceed 2⋅105.

OUTPUT FORMAT (print output to the terminal / stdout):
Output T lines, one line per test case.
If it possible to make all cows like the same type of hay simultaneously, output all possible such types of hay in increasing order. Otherwise, output −1. When printing a list of numbers on the same line, separate adjacent numbers with a space, and be sure the line does not end with any extraneous spaces.

SAMPLE INPUT:
5
5
1 2 2 2 3
6
1 2 3 1 2 3
6
1 1 1 2 2 2
3
3 2 3
2
2 1
SAMPLE OUTPUT:
2
-1
1 2
3
-1
In the sample input, there are 5 test cases.

In the first test case, it is only possible to make all cows like type 2. FJ can do this by running a single focus group with all cows.

In the second test case, we can show that no cows will change which type of hay they like.

In the third test case, it is possible to make all cows like type 1 by running three focus groups - first by having cows 1 through 4 in a focus group, then by having cows 1 through 5 in a focus group, then by having cows 1 through 6 in a focus group. By similar logic, using cows 3 through 6, cows 2 through 6, then cows 1 through 6, we can make all cows like type 2.

In the fourth test case, it is possible to make all cows like type 3 by running a single focus group with all cows.

In the fifth test case, we can show that no cows will change which type of hay they like.

SCORING:
Input 2: N=2.
Inputs 3-4: N≤50.
Inputs 5-6: hi≤hi+1 for all 1≤i≤N−1.
Inputs 7-15: No additional constraints.

Problem credits: Nick Wu