LeetCode : Count Nice pairs in Array
====================================


문제설명
------

You are given an array nums that consists of non-negative integers.   
Let us define rev(x) as the reverse of the non-negative integer x.    
For example, rev(123) = 321, and rev(120) = 21. A pair of indices (i, j) is nice if it satisfies all of the following conditions:   
  
  0 <= i < j < nums.length   
  nums[i] + rev(nums[j]) == nums[j] + rev(nums[i])   
  
Return the number of nice pairs of indices. Since that number can be too large, return it modulo 109 + 7.   


문제풀이
------

해당 문제는 문제가 시키는데로 2중 for문을 사용해 문제를 풀면 시간초과로 인해 해결할 수 없다.   
단일 for문을 이용해 해결하는 것이 **key point** 이다. 단일 for문을 이용하기 위해서는 위의 condition을 조금만 조정해 주면 된다.   
해당식 nums[i] + rev(nums[j]) == nums[j] + rev(nums[i]) 이것을 nums[i] - rev(nums[i]) == nums[j] - rev(nums[j])


