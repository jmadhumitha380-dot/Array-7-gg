# Array-7-gg
Practice program
class Solution:
    def findTwoElement(self, arr):
        n = len(arr)
        seen = set()
        duplicate = -1

        # Find duplicate
        for num in arr:
            if num in seen:
                duplicate = num
            else:
                seen.add(num)

        # Find missing
        missing = -1
        for i in range(1, n + 1):
            if i not in seen:
                missing = i
                break

        return [duplicate, missing]
Output:
Input: 
arr[] =
2 2
Your Output:
[2, 1]
