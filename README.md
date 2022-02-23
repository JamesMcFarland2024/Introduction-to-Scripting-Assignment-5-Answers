# Introduction-to-Scripting-Assignment-5-Answers
# Question 1 Answer
# Dictionary representing the morse code chart
MORSE_CODE_DICT = { 'A':'.-', 'B':'-...',
   'C':'-.-.', 'D':'-..', 'E':'.',
   'F':'..-.', 'G':'--.', 'H':'....',
   'I':'..', 'J':'.---', 'K':'-.-',
   'L':'.-..', 'M':'--', 'N':'-.',
   'O':'---', 'P':'.--.', 'Q':'--.-',
   'R':'.-.', 'S':'...', 'T':'-',
   'U':'..-', 'V':'...-', 'W':'.--',
   'X':'-..-', 'Y':'-.--', 'Z':'--..',
   '1':'.----', '2':'..---', '3':'...--',
   '4':'....-', '5':'.....', '6':'-....',
   '7':'--...', '8':'---..', '9':'----.',
   '0':'-----', ', ':'--..--', '.':'.-.-.-',
   '?':'..--..', '/':'-..-.', '-':'-....-',
   '(':'-.--.', ')':'-.--.-'
}
def encryption(message):
   my_cipher = ''
   for myletter in message:
      if myletter != ' ':
         my_cipher += MORSE_CODE_DICT[myletter] + ' '
      else:
         my_cipher += ' '
      return my_cipher
# This function is used to decrypt
# Morse code to English
def decryption(message):
   message += ' '
   decipher = ''
   mycitext = ''
   for myletter in message:
      # checks for space
      if (myletter != ' '):
         i = 0
         mycitext += myletter
      else:
         i += 1
         if i == 2 :
            decipher += ' '
         else:
            decipher += list(MORSE_CODE_DICT.keys())[list(MORSE_CODE_DICT
            .values()).index(mycitext)]
            mycitext = ''
   return decipher
def main():
   my_message = "PYTHON-PROGRAM"
   output = encryption(my_message.upper())
   print (output)
   my_message = ".--. -.-- - .... --- -.  -....- .--. .-. --- --. .-. .- -- "
   output = decryption(my_message)
   print (output)
# Executes the main function
if __name__ == '__main__':
   main()
   
# Question 2 Answer
# Python Program to Count Vowels and Consonants in a String
str1 = input("Please Enter Your Own String : ")
vowels = 0
consonants = 0
str1.lower()

for i in str1:
    if(i == 'a' or i == 'e' or i == 'i' or i == 'o' or i == 'u'):
        vowels = vowels + 1
    else:
        consonants = consonants + 1
 
print("Total Number of Vowels in this String = ", vowels)
print("Total Number of Consonants in this String = ", consonants)

# Question 3
# part 1: 8 letters, 4 symbols, 3 numbers
# Part 2: "Jon is developer musician"
# Part 3: "Emma is a data scientist"
# Part 4: 
# initializing string
test_str = "Hello have a good day"

# printing original string
print("The original string is : " + test_str)
 
# Remove all consonants from string
# Using loop
res = []
for chr in test_str:
    if chr in "aeiouAEIOU":
        res.extend(chr)
res = "".join(res)
 
# printing result
print("String after consonants removal : " + str(res))
