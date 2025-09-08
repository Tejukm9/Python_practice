---
generator: Aspose.Words for Java 23.4.0;
---

Topic 1: Variables & Input

****Challenge 1.1: Write a program that: Asks the user for their first
name and last name Then prints: Hello FirstName LastName!****

Code\
fname = input(\"Enter your first name: \")\
lname = input(\"Enter your last name: \")\
print(f\"Hello {fname} {lname}!\")

**Challenge 1.2: Ask the user for their favorite color and favorite
food, then print: Your dream dinner is \[food\] on a \[color\] plate.**

Code\
favcl = input(\"What\'s your favorite color? \")\
favf = input(\"What\'s your favorite food? \")\
print(f\"Your dream dinner is {favf} on a {favcl} plate.\")

**Challenge 1.3: Ask the user for their birth year, then calculate and
print their age in 2025.**

Code\
age_in = int(input(\"What\'s your birth year? \"))\
age = 2025 - age_in\
print(f\"In 2025, you will be {age} years old.\")

**Challenge 1.4: Ask the user for their birth year. If invalid, print an
error; otherwise print their age in 2025.**

Code\
try:\
age_in = int(input(\"What\'s your birth year? \"))\
age = 2025 - age_in\
print(f\"In 2025, you will be {age} years old.\")\
except ValueError:\
print(\"Please enter a valid year.\")

**Challenge 1.5: Ask the user for their current age and a number of
years in the future; print their future age.**

Code\
try:\
age_now = int(input(\"What is your current age? \"))\
years = int(input(\"How many years in the future do you want to see?
\"))\
future_age = age_now + years\
print(f\"In {years} years, you will be {future_age} years old.\")\
except ValueError:\
print(\"Please enter a valid number for age and years.\")

**Challenge 1.6: Ask the user for two integers and print their sum,
difference, product, and quotient (if the second isn\'t zero).**

Code\
try:\
x = int(input(\"Enter integer x: \"))\
y = int(input(\"Enter integer y: \"))\
print(f\"sum = {x + y}\")\
print(f\"difference = {x - y}\")\
print(f\"product = {x \* y}\")\
if y == 0:\
print(\"Cannot divide by 0\")\
else:\
print(f\"divide = {x / y}\")\
except ValueError:\
print(\"Please enter valid integers.\")

**Challenge 1.7: Ask for a temperature in Celsius, convert to
Fahrenheit, and print the result.**

Code\
try:\
cel = float(input(\"Enter the temperature in Celsius: \"))\
far = (cel \* 9/5) + 32\
print(f\"{cel}°C is {round(far, 1)}°F\")\
except ValueError:\
print(\"Enter a valid number.\")

**Challenge 1.8: Ask the user to enter a sentence, then print the
character count, word count, and the reversed sentence.**

Code\
line = input(\"Enter a sentence: \")\
print(f\"Characters: {len(line)}\")\
print(f\"Words: {len(line.split())}\")\
print(f\"Reversed: {line\[::-1\]}\")

**Challenge 1.9: Ask the user for a word and print whether it is a
palindrome.**

Code\
pal = input(\"Enter a word: \")\
if pal == pal\[::-1\]:\
print(f\"The word \'{pal}\' is a palindrome.\")\
else:\
print(f\"The word \'{pal}\' is not a palindrome.\")

**Challenge 1.10: Ask for two words and print True if they are anagrams
(case-insensitive), else False.**

Code\
word_1 = input(\"Enter first word: \")\
word_2 = input(\"Enter second word: \")\
print(sorted(word_1.lower()) == sorted(word_2.lower()))

Topic 2: Data Types & Type Casting

**Challenge 2.1: Ask the user to enter a number, convert it to a float,
and print both.**

Code\
fl = float(input(\"Enter a number: \"))\
print(f\"You entered {fl} and as a float it\'s {float(fl)}\")

**Challenge 2.2: Ask the user for a decimal number, then print it as
float and as integer using int() (truncates).**

Code\
fl = float(input(\"Enter a number: \"))\
integer = int(fl)\
print(f\"As float: {fl}\\nAs integer: {integer}\")

**Challenge 2.3: Ask the user for their name and age; print both and
their age in 5 years (use casting).**

Code\
name = input(\"Enter your name: \")\
age = int(input(\"Enter your age: \"))\
age_5 = age + 5\
print(f\"Hello {name}! You are {age} years old.\")\
print(f\"In 5 years, you\'ll be {age_5}.\")

**Challenge 2.4: Ask for two (possibly decimal) numbers, multiply, and
print the result rounded to 2 decimals.**

Code\
n1 = float(input(\"Enter first number: \"))\
n2 = float(input(\"Enter second number: \"))\
prod = n1 \* n2\
print(f\"Result: {round(prod, 2)}\")

**Challenge 2.5: Ask for a number and print whether it is even or odd.**

Code\
n1 = float(input(\"Enter a number: \"))\
print(f\"{n1} is even\" if int(n1) % 2 == 0 else f\"{n1} is odd\")

**Challenge 2.6: Ask for any input, convert to bool, and print the
result.**

Code\
ty = input(\"Enter anything: \").strip()\
print(f\"You entered \'{ty}\', which is considered {bool(ty)}\")

**Challenge 2.7: Ask for an integer and a float, add them, and print the
result and its type.**

Code\
n1 = int(input(\"Enter an integer: \"))\
f1 = float(input(\"Enter a float: \"))\
ad = n1 + f1\
print(f\"Result: {ad}\")\
print(f\"Type: {type(ad)}\")

**Challenge 2.8: Ask for any input; if it can be converted to float,
print the value; otherwise say it cannot be converted.**

Code\
n1 = input(\"Enter anything: \")\
print(f\"Type: {type(n1)}\")\
try:\
f = float(n1)\
print(f\"Converted to float: {f}\")\
except ValueError:\
print(f\"Cannot convert \'{n1}\' to float\")

**Challenge 2.9: Ask for a number (as string) and a word; repeat the
word that many times.**

Code\
n1 = int(input(\"Enter a number: \"))\
w1 = input(\"Enter a word: \")\
print(w1 \* n1)

**Challenge 2.10: Mini calculator: ask for two numbers and an operation
(+, -, \*, /). Compute with rounding; guard divide-by-zero.**

Code\
try:\
n1 = float(input(\"Enter first number: \"))\
n2 = float(input(\"Enter second number: \"))\
op = input(\"Enter the operation (+, -, \*, /): \").strip()\
if op == \"\*\":\
print(f\"The product is {round(n1 \* n2, 2)}\")\
elif op == \"+\":\
print(f\"The sum is {round(n1 + n2, 2)}\")\
elif op == \"-\":\
print(f\"The difference is {round(n1 - n2, 2)}\")\
elif op == \"/\":\
if n2 == 0:\
print(f\"{n2} is not a viable value for this operation\")\
else:\
print(f\"The div is {round(n1 / n2, 2)}\")\
else:\
print(\"Unknown operation.\")\
except ValueError:\
print(\"Enter valid numbers.\")

Topic 3: Strings

**Challenge 3.1: Ask for an integer and say whether it's odd/even and
positive/negative/zero.**

Code\
try:\
ni = int(input(\"Enter an integer: \"))\
if ni == 0:\
print(f\"{ni} is neither odd nor even\")\
elif ni % 2 == 0 and ni \> 0:\
print(f\"{ni} is even number and positive\")\
elif ni % 2 == 0 and ni \< 0:\
print(f\"{ni} is even number and negative\")\
elif ni % 2 != 0 and ni \< 0:\
print(f\"{ni} is odd number and negative\")\
else:\
print(f\"{ni} is odd number and positive\")\
except ValueError:\
print(\"Enter a valid integer\")

**Challenge 3.2: Grading system: map score 0--00 to A/B/C/D/F; reject
out-of-range.**

Code\
try:\
ni = int(input(\"Enter your score (0--00): \"))\
if ni \< 0 or ni \> 100:\
print(\"Enter a valid score between 0 and 100.\")\
elif ni \>= 90:\
print(\"Grade: A\")\
elif ni \>= 80:\
print(\"Grade: B\")\
elif ni \>= 70:\
print(\"Grade: C\")\
elif ni \>= 60:\
print(\"Grade: D\")\
else:\
print(\"Grade: F\")\
except ValueError:\
print(\"Please enter a valid number.\")

**Challenge 3.3: Movie ticket pricing by age: free (\<5), child (5--2),
adult (13--9), senior (60+), invalid if negative.**

Code\
try:\
age = int(input(\"Enter your age: \"))\
if age \< 0:\
print(\"Invalid age.\")\
elif age \>= 60:\
print(\"Senior ticket: \$7\")\
elif age \> 12:\
print(\"Adult ticket: \$12\")\
elif age \>= 5:\
print(\"Child ticket: \$5\")\
else:\
print(\"Ticket is free!\")\
except ValueError:\
print(\"Enter a valid number\")

**Challenge 3.4: Ask for three numbers; print the largest or say that
the largest value is shared.**

Code\
try:\
n1 = int(input(\"Enter number 1: \"))\
n2 = int(input(\"Enter number 2: \"))\
n3 = int(input(\"Enter number 3: \"))\
if n1 == n2 == n3:\
print(\"All numbers are equal.\")\
else:\
max_val = max(n1, n2, n3)\
count = \[n1, n2, n3\].count(max_val)\
if count \> 1:\
print(\"Two or more numbers share the highest value.\")\
else:\
print(f\"{max_val} is the largest number.\")\
except ValueError:\
print(\"Enter a valid number.\")

**Challenge 3.5: Leap year checker: divisible by 4 and (not by 100 or by
400).**

Code\
try:\
year = int(input(\"Enter a year: \"))\
if (year % 4 == 0) and (year % 100 != 0 or year % 400 == 0):\
print(f\"{year} is a leap year\")\
else:\
print(f\"{year} is not a leap year\")\
except ValueError:\
print(\"Please enter a valid year.\")

Topic 4: Lists & Loops

**Challenge 4.1: Multiplication table (1 to 10) for an input number.**

Code\
n1 = int(input(\"Enter a number: \"))\
for x in range(1, 11):\
print(f\"{n1} x {x} = {n1 \* x}\")

**Challenge 4.2: Right-angled triangle pattern of \* up to n rows.**

Code\
n = int(input(\"Enter a number: \"))\
for x in range(1, n + 1):\
print(\"\*\" \* x)

**Challenge 4.3: Keep asking for numbers and sum them until the user
enters 0; then print the total.**

Code\
tot = 0\
while True:\
y = int(input(\"Enter a number (0 to stop): \"))\
if y == 0:\
break\
tot += y\
print(f\"Total sum is: {tot}\")

**Challenge 4.4: Number guessing game (1--0) with feedback (too
low/high) until correct.**

Code\
from random import randint\
x = randint(1, 10)\
while True:\
y = int(input(\"Guess the number (1--0): \"))\
if y \< x:\
print(\"Too low!\")\
elif y \> x:\
print(\"Too high!\")\
else:\
print(\"You got it!\")\
break

**Challenge 4.5: Reverse a string manually using a loop (no
slicing/reversed).**

Code\
text = input(\"Enter a word: \")\
reversed_text = \"\"\
for i in range(len(text) - 1, -1, -1):\
reversed_text += text\[i\]\
print(f\"Reversed: {reversed_text}\")

**Challenge 4.6: Count vowels (a, e, i, o, u) in a sentence
(case-insensitive).**

Code\
sen = input(\"Enter a sentence: \")\
x = 0\
for i in sen.lower():\
if i in \"aeiou\":\
x += 1\
print(f\"Total number of vowels: {x}\")

**Challenge 4.7: Print all even numbers in a given inclusive range (skip
0 if desired).**

Code\
x = int(input(\"Enter a start number: \"))\
y = int(input(\"Enter the end number: \"))\
print(\"Even numbers:\")\
for i in range(x, y + 1):\
if i % 2 == 0 and i != 0:\
print(i)

**Challenge 4.8: Sum the digits of a positive integer.**

Code\
pn = int(input(\"Enter a positive number: \"))\
tot = 0\
for digit in str(pn):\
tot += int(digit)\
print(f\"Sum of digits: {tot}\")

**Challenge 4.9: FizzBuzz from 1 to 50 (Fizz for 3, Buzz for 5, FizzBuzz
for both).**

Code\
for i in range(1, 51):\
if i % 3 == 0 and i % 5 == 0:\
print(\"FizzBuzz\")\
elif i % 5 == 0:\
print(\"Buzz\")\
elif i % 3 == 0:\
print(\"Fizz\")\
else:\
print(i)

**Challenge 4.10: Prime number checker using a loop; numbers \< 2 are
not prime.**

Code\
x = int(input(\"Enter a positive integer: \"))\
if x \< 2:\
print(f\"{x} is not a prime number\")\
else:\
for i in range(2, x):\
if x % i == 0:\
print(f\"{x} is not a prime number\")\
break\
else:\
print(f\"{x} is a prime number\")

Topic 5: Dictionaries & Sets

**Challenge 5.1: Create a list of favorites, print first/last, append
one item, and print the updated list.**

Code\
favorites = \[\"red\", \"laptop\", \"car\"\]\
print(favorites)\
print(\"First:\", favorites\[0\])\
print(\"Last:\", favorites\[-1\])\
favorites.append(\"house\")\
print(\"Updated list:\", favorites)

**Challenge 5.2: Start with 5 items; replace the 3rd item (index 2);
print updated list and its length.**

Code\
fav = \[\"red\", \"laptop\", \"car\", \"house\", \"game\"\]\
print(fav)\
fav\[2\] = \"school\"\
print(fav)\
print(f\"length: {len(fav)}\")

**Challenge 5.3: Remove the second item with del, pop the last item, and
print results.**

Code\
fav = \[\"red\", \"laptop\", \"car\", \"house\", \"game\"\]\
print(\"Original list:\", fav)\
del(fav\[1\])\
print(\"After del:\", fav)\
print(\"Removed with pop():\", fav.pop())\
print(\"Final list:\", fav)

**Challenge 5.4: Sort a list, then reverse it; print after each step.**

Code\
fav = \[\"red\", \"laptop\", \"car\", \"house\", \"game\"\]\
print(fav)\
fav.sort()\
print(fav)\
fav.reverse()\
print(fav)

**Challenge 5.5: Check if a guessed integer is in a list of numbers.**

Code\
fav = \[1, 2, 3, 4, 5\]\
gues = int(input(\"Enter an integer: \"))\
if gues in fav:\
print(\"Your guess is correct.\")\
else:\
print(\"Your guess is wrong.\")

Topic 6: Functions

**Challenge 6.1: Ask for a sentence, then print
original/upper/lower/no-spaces/length (no spaces).**

Code\
sen = input(\"Enter a sentence: \")\
print(f\"Original: {sen}\")\
print(f\"Uppercase: {sen.upper()}\")\
print(f\"Lowercase: {sen.lower()}\")\
space_less = sen.replace(\" \", \"\")\
print(f\"No spaces: {space_less}\")\
print(f\"Length (no spaces): {len(space_less)}\")

**Challenge 6.2: Ask for a word; print first, last, middle (1 or 2
chars), and the reversed word.**

Code\
sen = input(\"Enter a word: \")\
print(f\"First: {sen\[0\]}\")\
print(f\"Last: {sen\[-1\]}\")\
l = len(sen)\
mid = l // 2\
if l % 2 == 0:\
print(f\"Middle: {sen\[mid-1:mid+1\]}\")\
else:\
print(f\"Middle: {sen\[mid\]}\")\
print(f\"Reversed: {sen\[::-1\]}\")

**Challenge 6.3: Ask for a sentence and a search word; print word count
and occurrences (case-insensitive).**

Code\
sen = input(\"Enter a sentence: \")\
ser = input(\"Enter a word to search: \")\
word_list = sen.split()\
print(f\"Word count: {len(word_list)}\")\
count = 0\
for word in word_list:\
if word.lower() == ser.lower():\
count += 1\
print(f\"\\\"{ser}\\\" appears {count} times in the sentence.\")

**Challenge 6.4: Mask a name by replacing all letters except the first
and last with \* (short names unchanged).**

Code\
name = input(\"Enter your full name: \")\
if len(name) \<= 2:\
print(f\"Masked: {name}\")\
else:\
mid = \"\*\" \* (len(name) - 2)\
print(f\"Masked: {name\[0\]}{mid}{name\[-1\]}\")

**Challenge 6.5: Convert a sentence to title case (capitalize each
word).**

Code\
sen = input(\"Enter a sentence: \")\
print(\" \".join(word.capitalize() for word in sen.split()))

**Challenge 6.6: Count vowels in a sentence (a, e, i, o, u).**

Code\
sen = input(\"Enter a sentence: \")\
x = 0\
for i in sen.lower():\
if i in \"aeiou\":\
x += 1\
print(f\"Total number of vowels: {x}\")

**Challenge 6.7: Remove punctuation from a sentence and print the
cleaned string.**

Code\
import string\
sen = input(\"Enter a sentence: \")\
x = \"\"\
for i in sen:\
if i not in string.punctuation:\
x += i\
print(f\"Cleaned sentence: {x}\")

**Challenge 6.8: Count how many times each character appears (ignore
spaces).**

Code\
sentence = input(\"Enter a sentence: \")\
counts = {}\
for char in sentence:\
if char != \" \":\
counts\[char\] = counts.get(char, 0) + 1\
for k, v in counts.items():\
print(f\"{k}: {v}\")

**Challenge 6.9: Replace all instances of a word with another
(case-sensitive).**

Code\
sentence = input(\"Enter a sentence: \")\
old = input(\"Word to replace: \")\
new = input(\"Replace with: \")\
print(\"Updated sentence:\", sentence.replace(old, new))

**Challenge 6.10: Mini Project ---Word Statistics Analyzer: characters
(no spaces/punct),** **word count, most frequent word, title case, and
replacement.**

Code\
import string\
par = input(\"Enter a paragraph: \")\
no_spc = \"\".join(c for c in par if c not in string.whitespace +
string.punctuation)\
print(f\"Number of characters (no spaces/punctuation): {len(no_spc)}\")\
words = par.split()\
print(f\"Number of words: {len(words)}\")\
rep = {}\
for word in par.lower().split():\
clean_word = word.strip(string.punctuation)\
rep\[clean_word\] = rep.get(clean_word, 0) + 1\
most_freq_word = max(rep, key=rep.get)\
print(f\"Most frequent word is \'{most_freq_word}\'
({rep\[most_freq_word\]} times)\")\
print(\"Title case:\")\
print(par.title())\
repl = input(\"Enter word to replace: \")\
replacer = input(\"Enter word to replace it with: \")\
print(\"Replaced paragraph:\")\
print(par.replace(repl, replacer))

Topic 7: Problem-Solving Projects

**Challenge 7.1: Power Function (no \*\*): Implement power(base,
exponent) with a loop; handle negative exponents and exponent 0.**

Code\
def power(base, exponent):\
result = 1\
for \_ in range(abs(exponent)):\
result \*= base\
return 1 / result if exponent \< 0 else result

**Challenge 7.2: Custom Joiner (no str.join): custom\_join(separator,
words) to join items without using str.join().**

Code

def custom_join(separator, words):\
sentence = \"\"\
for i in range(len(words)):\
sentence += words\[i\]\
if i != len(words) - 1:\
sentence += separator\
return sentence

**Challenge 7.3: Character Frequency (case-insensitive): Return a dict
of character counts (keep spaces and punctuation).**

Code

def char_frequency(text):\
counts = {}\
for ch in text.lower():\
counts\[ch\] = counts.get(ch, 0) + 1\
return counts

**Challenge 7.4: Custom Split (no str.split): custom\_split(text,
delimiter) to return substrings split by delimiter.**

Code

def custom_split(text, delimiter):\
parts = \[\]\
current = \"\"\
for ch in text:\
if ch == delimiter:\
parts.append(current)\
current = \"\"\
Else:\
current += ch\
if current:\
parts.append(current)\
return parts

**Challenge 7.5: Capitalize Sentences: Capitalize the first alphabetic
character after \'.\', \'!\' or \'?\' and at the start.**

Code

def capitalize_sentences(text):\
result = \"\"\
cap_next = True\
for ch in text:\
if cap_next and ch.isalpha():\
result += ch.upper()\
cap_next = False\
Else:\
result += ch\
if ch in \".!?\":\
cap_next = True\
return result

**Challenge 7.6: Acronym Generator: generate\_acronym(phrase) using the
first letters of significant words (skip and/of/in/the/a).**

Code

def generate_acronym(text):\
stop = {\'and\', \'of\', \'in\', \'the\', \'a\'}\
letters = \[\]\
for word in text.split():\
if word.lower() not in stop and word:\
letters.append(word\[0\].upper())\
return \"\".join(letters)

Challenge 7.7: Anagram Checker: is_anagram(w1, w2) returns True if the
words are anagrams (ignore spaces and case).

Code

def is_anagram(word1, word2):\
w1 = word1.lower().replace(\" \", \"\")\
w2 = word2.lower().replace(\" \", \"\")\
d1, d2 = {}, {}\
for ch in w1:\
d1\[ch\] = d1.get(ch, 0) + 1\
for ch in w2:\
d2\[ch\] = d2.get(ch, 0) + 1\
return d1 == d2

**Challenge 7.8: Word Count (ignore punctuation, case-insensitive):
word\_count(text) returns a dict of word frequencies.**

Code

import string\
def word_count(text):\
cleaned = text.lower().translate(str.maketrans(\"\", \"\",
string.punctuation))\
counts = {}\
for word in cleaned.split():\
counts\[word\] = counts.get(word, 0) + 1\
return counts

**Challenge 7.9: Pangram Checker: is\_pangram(text) returns True if text
contains every letter a--z at least once.**

Code

import string\
def is_pangram(text):\
alphabet = set(string.ascii_lowercase)\
cleaned = (text.lower()\
.translate(str.maketrans(\"\", \"\", string.punctuation))\
.replace(\" \", \"\"))\
return alphabet.issubset(set(cleaned))

**Challenge 7.10: Mini Project ---Text Analyzer: analyze\_text(text)
returns total\_characters (no spaces/punct), total\_words,
unique\_words, most\_common\_word, vowel\_count, is\_pangram.**

Code

import string\
def analyze_text(text):\
analysis = {}\
cleaned = text.lower().translate(str.maketrans(\"\", \"\",
string.punctuation))\
no_space = cleaned.replace(\" \", \"\")\
words = cleaned.split()

\# word frequencies

freq = {}\
for w in words:\
freq\[w\] = freq.get(w, 0) + 1

\# fill analysis\
analysis\[\"total_characters\"\] = len(no_space)\
analysis\[\"total_words\"\] = len(words)\
analysis\[\"unique_words\"\] = len(set(words))\
analysis\[\"most_common_word\"\] = max(freq, key=freq.get) if freq else
None\
vowels = \"aeiou\"\
analysis\[\"vowel_count\"\] = sum(1 for ch in no_space if ch in vowels)\
alphabet = set(string.ascii_lowercase)\
analysis\[\"is_pangram\"\] = alphabet.issubset(set(no_space))

return analysis
