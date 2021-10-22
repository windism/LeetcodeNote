
# 位运算

## 位运算技巧

**异或特性**

```text
x ^ 0 = x
x ^ 1111....11111 = ~x
x ^ (~x) = 11111....1111
x ^ x = 0
a ^ b = c => a ^ c = b  => b ^ c = a (交换律)
a ^ b ^ c = a ^ (b ^ c) = (a ^ b）^ c (结合律)
```

**最低位操作**

```text
# 判断是否是奇数(偶数)
X & 1 == 1 
# 最低位(LSB)的 1 清零
X & = (X - 1)
# 获得最低位(LSB)的 1
X & -X
X & ~X = 0
```

**特殊数据构造**

```text
# 将 x 最右边的 n 位清零
x & ( ~0 << n )
# 获取 x 的第 n 位值(0 或者 1)
(x >> n) & 1
# 获取 x 的第 n 位的幂值
x & (1 << (n - 1))
# 仅将第 n 位置为 1
x | (1 << n)
# 仅将第 n 位置为 0
x & (~(1 << n))
# 将 x 最高位至第 n 位(含)清零
x & ((1 << n) - 1)
# 将第 n 位至第 0 位(含)清零
x & (~((1 << (n + 1)) - 1)）
```

## 题目列表

| **#** | **Title**                                                          | **Acceptance** | **Difficulty** | **Favorite** |
|:-----:|:------------------------------------------------------------------:|:--------------:|:--------------:|:------------:|
| 29    | Divide Two Integers                                                | 17.0%          | Medium         |              |
| 67    | Add Binary                                                         | 48.8%          | Easy           |              |
| 78    | Subsets                                                            | 68.3%          | Medium         |              |
| 89    | Gray Code                                                          | 54.2%          | Medium         |              |
| 90    | Subsets II                                                         | 51.4%          | Medium         |              |
| 136   | [Single Number](../solution/0001_0999/0136.%20Single%20Number.md)  | 67.8%          | Easy           |              |
| 137   | [Single Number II](../solution/0001_0999/0137.%20Single%20Number%20II.md) | 55.4%          | Medium         |              |
| 187   | Repeated DNA Sequences                                             | 43.0%          | Medium         |              |
| 190   | Reverse Bits                                                       | 45.6%          | Easy           |              |
| 191   | [Number of 1 Bits](../solution/0001_0999/0191.%20Number%20of%201%20Bits.md) | 56.9%          | Easy           |              |
| 201   | Bitwise AND of Numbers Range                                       | 41.1%          | Medium         |              |
| 231   | Power of Two                                                       | 44.0%          | Easy           |              |
| 260   | [Single Number III](../solution/0001_0999/0260.%20Single%20Number%20III.md) | 65.8%          | Medium         |              |
| 266   | Palindrome Permutation                                             | 64.0%          | Easy           |              |
| 268   | Missing Number                                                     | 57.6%          | Easy           |              |
| 287   | Find the Duplicate Number                                          | 58.2%          | Medium         |              |
| 318   | Maximum Product of Word Lengths                                    | 55.9%          | Medium         |              |
| 320   | Generalized Abbreviation                                           | 55.1%          | Medium         |              |
| 338   | [Counting Bits](../solution/0001_0999/0338.%20Counting%20Bits.md) | 71.9%          | Easy           |              |
| 342   | Power of Four                                                      | 42.8%          | Easy           |              |
| 371   | Sum of Two Integers                                                | 50.7%          | Medium         |              |
| 389   | Find the Difference                                                | 58.8%          | Easy           |              |
| 393   | UTF-8 Validation                                                   | 38.8%          | Medium         |              |
| 397   | Integer Replacement                                                | 34.1%          | Medium         |              |
| 401   | Binary Watch                                                       | 49.6%          | Easy           |              |
| 405   | Convert a Number to Hexadecimal                                    | 45.3%          | Easy           |              |
| 411   | Minimum Unique Word Abbreviation                                   | 37.9%          | Hard           |              |
| 421   | Maximum XOR of Two Numbers in an Array                             | 55.0%          | Medium         |              |
| 461   | Hamming Distance                                                   | 73.6%          | Easy           |              |
| 464   | Can I Win                                                          | 29.6%          | Medium         |              |
| 473   | Matchsticks to Square                                              | 40.2%          | Medium         |              |
| 476   | Number Complement                                                  | 65.4%          | Easy           |              |
| 477   | Total Hamming Distance                                             | 51.4%          | Medium         |              |
| 491   | Increasing Subsequences                                            | 49.5%          | Medium         |              |
| 526   | Beautiful Arrangement                                              | 63.3%          | Medium         |              |
| 638   | Shopping Offers                                                    | 54.1%          | Medium         |              |
| 645   | Set Mismatch                                                       | 41.1%          | Easy           |              |
| 672   | Bulb Switcher II                                                   | 50.8%          | Medium         |              |
| 691   | Stickers to Spell Word                                             | 46.4%          | Hard           |              |
| 693   | Binary Number with Alternating Bits                                | 60.5%          | Easy           |              |
| 698   | Partition to K Equal Sum Subsets                                   | 45.8%          | Medium         |              |
| 751   | IP to CIDR                                                         | 56.1%          | Medium         |              |
| 756   | Pyramid Transition Matrix                                          | 55.6%          | Medium         |              |
| 762   | Prime Number of Set Bits in Binary Representation                  | 65.7%          | Easy           |              |
| 779   | K-th Symbol in Grammar                                             | 39.4%          | Medium         |              |
| 782   | Transform to Chessboard                                            | 51.8%          | Hard           |              |
| 784   | Letter Case Permutation                                            | 70.4%          | Medium         |              |
| 805   | Split Array With Same Average                                      | 26.6%          | Hard           |              |
| 810   | Chalkboard XOR Game                                                | 51.8%          | Hard           |              |
| 847   | Shortest Path Visiting All Nodes                                   | 55.4%          | Hard           |              |
| 861   | Score After Flipping Matrix                                        | 74.4%          | Medium         |              |
| 864   | Shortest Path to Get All Keys                                      | 43.4%          | Hard           |              |
| 868   | Binary Gap                                                         | 61.5%          | Easy           |              |
| 898   | Bitwise ORs of Subarrays                                           | 36.1%          | Medium         |              |
| 943   | Find the Shortest Superstring                                      | 45.6%          | Hard           |              |
| 957   | Prison Cells After N Days                                          | 39.8%          | Medium         |              |
| 980   | Unique Paths III                                                   | 77.6%          | Hard           |              |
| 982   | Triples with Bitwise AND Equal To Zero                             | 57.3%          | Hard           |              |
| 995   | Minimum Number of K Consecutive Bit Flips                          | 50.4%          | Hard           |              |
| 996   | Number of Squareful Arrays                                         | 49.0%          | Hard           |              |
| 1009  | Complement of Base 10 Integer                                      | 61.2%          | Easy           |              |
| 1066  | Campus Bikes II                                                    | 54.6%          | Medium         |              |
| 1256  | Encode Number                                                      | 69.0%          | Medium         |              |
| 1125  | Smallest Sufficient Team                                           | 47.5%          | Hard           |              |
| 1177  | Can Make Palindrome from Substring                                 | 36.8%          | Medium         |              |
| 1178  | Number of Valid Words for Each Puzzle                              | 41.0%          | Hard           |              |
| 1238  | Circular Permutation in Binary Representation                      | 67.7%          | Medium         |              |
| 1239  | Maximum Length of a Concatenated String with Unique Characters     | 50.6%          | Medium         |              |
| 1255  | Maximum Score Words Formed by Letters                              | 71.2%          | Hard           |              |
| 1284  | Minimum Number of Flips to Convert Binary Matrix to Zero Matrix    | 70.7%          | Hard           |              |
| 1310  | XOR Queries of a Subarray                                          | 70.6%          | Medium         |              |
| 1318  | Minimum Flips to Make a OR b Equal to c                            | 64.6%          | Medium         |              |
| 1342  | Number of Steps to Reduce a Number to Zero                         | 85.6%          | Easy           |              |
| 1356  | Sort Integers by The Number of 1 Bits                              | 70.7%          | Easy           |              |
| 1349  | Maximum Students Taking Exam                                       | 45.7%          | Hard           |              |
| 1371  | Find the Longest Substring Containing Vowels in Even Counts        | 62.0%          | Medium         |              |
| 1386  | Cinema Seat Allocation                                             | 37.6%          | Medium         |              |
| 1404  | Number of Steps to Reduce a Number in Binary Representation to One | 50.5%          | Medium         |              |
| 1434  | Number of Ways to Wear Different Hats to Each Other                | 41.0%          | Hard           |              |
| 1442  | Count Triplets That Can Form Two Arrays of Equal XOR               | 73.7%          | Medium         |              |
| 1461  | Check If a String Contains All Binary Codes of Size K              | 54.4%          | Medium         |              |
| 1457  | Pseudo-Palindromic Paths in a Binary Tree                          | 68.0%          | Medium         |              |
| 1494  | Parallel Courses II                                                | 31.1%          | Hard           |              |
| 1486  | XOR Operation in an Array                                          | 84.0%          | Easy           |              |
| 1525  | Number of Good Ways to Split a String                              | 70.6%          | Medium         |              |
| 1521  | Find a Value of a Mysterious Function Closest to Target            | 43.6%          | Hard           |              |
| 1506  | Find Root of N-Ary Tree                                            | 78.7%          | Medium         |              |
| 1542  | Find Longest Awesome Substring                                     | 39.7%          | Hard           |              |
| 1595  | Minimum Cost to Connect Two Groups of Points                       | 44.4%          | Hard           |              |
| 1601  | Maximum Number of Achievable Transfer Requests                     | 49.7%          | Hard           |              |
| 1611  | Minimum One Bit Operations to Make Integers Zero                   | 61.5%          | Hard           |              |
| 1617  | Count Subtrees With Max Distance Between Cities                    | 64.5%          | Hard           |              |
| 1655  | Distribute Repeating Integers                                      | 40.7%          | Hard           |              |
| 1659  | Maximize Grid Happiness                                            | 36.7%          | Hard           |              |
| 1684  | Count the Number of Consistent Strings                             | 81.8%          | Easy           |              |
| 1681  | Minimum Incompatibility                                            | 36.4%          | Hard           |              |
| 1680  | Concatenation of Consecutive Binary Numbers                        | 52.4%          | Medium         |              |
| 1723  | Find Minimum Time to Finish All Jobs                               | 41.8%          | Hard           |              |
| 1707  | Maximum XOR With an Element From Array                             | 42.6%          | Hard           |              |
| 1734  | Decode XORed Permutation                                           | 58.6%          | Medium         |              |
| 1720  | Decode XORed Array                                                 | 85.7%          | Easy           |              |
| 1738  | Find Kth Largest XOR Coordinate Value                              | 62.6%          | Medium         |              |
| 1763  | Longest Nice Substring                                             | 61.5%          | Easy           |              |
| 1755  | Closest Subsequence Sum                                            | 35.7%          | Hard           |              |
| 1799  | Maximize Score After N Operations                                  | 46.5%          | Hard           |              |
| 1803  | Count Pairs With XOR in a Range                                    | 45.6%          | Hard           |              |
| 1787  | Make the XOR of All Segments Equal to Zero                         | 38.0%          | Hard           |              |
| 1815  | Maximum Number of Groups Getting Fresh Donuts                      | 39.9%          | Hard           |              |
| 1829  | Maximum XOR for Each Query                                         | 75.2%          | Medium         |              |
| 1835  | Find XOR Sum of All Pairs Bitwise AND                              | 57.7%          | Hard           |              |
| 1879  | Minimum XOR Sum of Two Arrays                                      | 39.2%          | Hard           |              |
| 1863  | Sum of All Subset XOR Totals                                       | 78.1%          | Easy           |              |
| 1915  | Number of Wonderful Substrings                                     | 40.6%          | Medium         |              |
| 1908  | Game of Nim                                                        | 59.4%          | Medium         |              |
| 1938  | Maximum Genetic Difference Query                                   | 38.4%          | Hard           |              |
| 1947  | Maximum Compatibility Score Sum                                    | 58.2%          | Medium         |              |
| 1994  | The Number of Good Subsets                                         | 32.1%          | Hard           |              |
| 1986  | Minimum Number of Work Sessions to Finish the Tasks                | 30.8%          | Medium         |              |
| 2002  | Maximum Product of the Length of Two Palindromic Subsequences      | 50.5%          | Medium         |              |
| 2035  | Partition Array Into Two Arrays to Minimize Sum Difference         | 23.6%          | Hard           |              |
| 2044  | Count Number of Maximum Bitwise-OR Subsets                         | 74.8%          | Medium         |              |
