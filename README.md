# GeekForGeeksPOTD
Maximum Value
class Node:
    def __init__(self, val):
        self.right = None
        self.data = val
        self.left = None
'''

class Solution:
    def maximumValue(self,node):
        # code here
         # code here
        ans = []
        m = -1
        q = deque([node,None])
        while True:
            x = q.popleft()
            if x:
                if x.left:
                    q.append(x.left)
                if x.right:
                    q.append(x.right)
                
                if x.data > m:
                    m = x.data
            else:
                ans.append(m)
                m = -1
                if q:
                    q.append(None)
                else:
                    return ans
