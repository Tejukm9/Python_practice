---
title: Python Beginner Challenges (1.1 to 7.9)
---

# Challenge 1.1 --- Greeting Program

Ask the user for their first and last name and print a greeting.

fname = input(\"Enter your first name: \")\
lname = input(\"Enter your last name: \")\
print(\"Hello \" + fname + \" \" + lname + \"!\")

# Challenge 7.7 --- Anagram Checker

Write a function to check if two words are anagrams.

def is_anagram(word1, word2):\
word1 = word1.lower().replace(\" \", \"\")\
word2 = word2.lower().replace(\" \", \"\")\
return sorted(word1) == sorted(word2)\
\
print(is_anagram(\"listen\", \"silent\"))
