### [169. 多数元素](https://leetcode.cn/problems/majority-element/)

Boyer-Moore 投票算法

- 用于寻找多数元素/主要元素（数量大于n/2）

- 基本思想：

- 代码：

  ```python 3
  class Solution:
      def majorityElement(self, nums: List[int]) -> int:
          count = 0
          candidate = None
  
          for num in nums:
              if count == 0:
                  candidate = num
              count += (1 if num == candidate else -1)
  
          return candidate
  ```

  

