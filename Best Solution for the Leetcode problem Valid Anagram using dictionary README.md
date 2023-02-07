echo "# Valid-Anagram" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/prac1312hi/Valid-Anagram.git
git push -u origin main

#Best Solution for the above problem using dictionary in python
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
