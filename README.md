<h1>Simple Encryption Maker Lab</h1>

<h2>Description</h2>
This is a simple Python script that takes inspiration from the common Caesar Cipher encryption model. The script first imports the string module. Next, it defines a function called "encrypt" which takes two parameters, the text to be encrypted and the key (shift value). Inside the function, it creates an empty string that will be used to store the encrypted text. It iterates through each character in the text, checking if the character is a letter, if true, it shifts the letter by the key using ord() and chr() functions. Then it adds the shifted letter to the encrypted text. Finally, it returns the encrypted text. It then tests the function by defining a text and key value and calls the function, encrypting the text, and printing the encrypted text.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 11</b>

<h2>Program Walkthrough:</h2>
 
 <b>Step 1: This line imports the string module which will be used to check if characters in the text are letters.</b>

```python
import string
```
<b>Step 2: This is the start of the function "encrypt" that takes in two arguments, "text" and "key". "text" is the text that will be encrypted and "key" is the number of positions each letter in the text will be shifted by.</b>

```python
def encrypt(text, key):
```

<b>Step 3: This line creates an empty string named "encrypted_text" that will be used to store the encrypted text.</b>

```python
encrypted_text = ""
```
<b>Step 4: This line starts a for loop that will iterate through each character in the text.</b>

```python
for char in text:
```
<b>Step 5: This line checks if the current character is a letter, if it is, the following block of code will execute.</b>

```python
if char.isalpha():
```
<b>Step 6: This line shifts the current letter by the key number of positions. The shift is done by converting the letter to its ASCII value, shifting it by the key, and converting it back to its letter form.</b>

```python
char = chr((ord(char) + key - 97) % 26 + 97)
```
<b>Step 7: This line adds the shifted letter to the "encrypted_text" string.</b>

```python
encrypted_text += char
```
<b>Step 8: This line returns the "encrypted_text" string which contains the encrypted text.</b>

```python
return encrypted_text
```

<b>Step 9: Test the Encryption Proces by displaying both the new translation and the old phrase given to compare.</b>

```python
 # Step 3: Test the encryption function
text = "Hey guys my name is Denal!"
key = 3
encrypted_text = encrypt(text, key)
print(encrypted_text)
print(text)
```
<b>The Final Result should look like this</b>
 
 ```python
 # Step 1: Import the necessary modules
import string

# Step 2: Define the encryption function
def encrypt(text, key):
    # Step 2.1: Create an empty string to store the encrypted text
    encrypted_text = ""
    # Step 2.2: Iterate through each character in the text
    for char in text:
        # Step 2.3: Check if the character is a letter
        if char.isalpha():
            # Step 2.4: Shift the letter by the key
            char = chr((ord(char) + key - 97) % 26 + 97)
        # Step 2.5: Add the shifted letter to the encrypted text
        encrypted_text += char
    # Step 2.6: Return the encrypted text
    return encrypted_text

# Step 3: Test the encryption function
text = "Hey guys my name is Denal!"
key = 3
encrypted_text = encrypt(text, key)
print(encrypted_text)
print(text)
```
