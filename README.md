# Assign-Cookies

class Solution:
    def findContentChildren(self, g, s):
        g.sort()
        s.sort()

        content_children = 0
        i, j = 0, 0  # Indices for greed factors and cookie sizes

        while i < len(g) and j < len(s):
            if s[j] >= g[i]:
                content_children += 1
                i += 1  # Move to the next child
            j += 1  # Move to the next available cookie

        return content_children

# Example usage
solution = Solution()

# Example 1
g1 = [1, 2, 3]
s1 = [1, 1]
print("Example 1:", solution.findContentChildren(g1, s1))

# Example 2
g2 = [1, 2]
s2 = [1, 2, 3]
print("Example 2:", solution.findContentChildren(g2, s2))
