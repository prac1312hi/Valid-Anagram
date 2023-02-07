# Valid-Anagram
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        d1 = Counter(s)
        d2=Counter(t)

        for key , val in d1.items():
            if key not in d2:
                return False
            if d2[key] < val:
                return False
        return True
