This is our hackathon project. It is a message encryptor-decryptor application made using python and tkinter. This applicaton takes up the message to be encrypted or decrypted then the mode e-encode, d-decode and the specific key that was used to encrypt the message. It ranges from 1-9.

1. `Encode(key, message)` function:
   - This function takes two parameters: `key` (the private key) and `message` (the input message to be encoded).
   - It initializes an empty list called `enc` to store the encoded characters.
   - It iterates over each character in the `message` using a `for` loop and assigns the corresponding character from the `key` using the modulo operator (`%`).
   - For each character in the `message`, it performs an encoding operation by adding the ASCII values of the `message` character and the corresponding `key` character, then takes the modulo 256 to ensure the result is within the valid ASCII range.
   - The encoded character is converted to a character using the `chr()` function and appended to the `enc` list.
   - After encoding all characters in the `message`, the `enc` list is joined into a single string, encoded using base64 encoding (`base64.urlsafe_b64encode()`), and finally decoded to a string using the `decode()` method.
   - The encoded and decoded result is returned.

2. `Decode(key, message)` function:
   - This function takes two parameters: `key` (the private key) and `message` (the input message to be decoded).
   - It initializes an empty list called `dec` to store the decoded characters.
   - The base64-encoded `message` is decoded using `base64.urlsafe_b64decode()` and then converted to a string using the `decode()` method.
   - It iterates over each character in the decoded message using a `for` loop and assigns the corresponding character from the `key` using the modulo operator (`%`).
   - For each character in the decoded message, it performs a decoding operation by subtracting the ASCII value of the `key` character from the ASCII value of the decoded message character, adding 256 to ensure the result is within the valid ASCII range.
   - The decoded character is converted to a character using the `chr()` function and appended to the `dec` list.
   - After decoding all characters in the message, the `dec` list is joined into a single string using the `"".join()` method and returned as the decoded result.

3. `Mode()` function:
   - This function is called when the user clicks the "RESULT" button.
   - It first checks the value of the `mode` variable, which is obtained from the input field where the user selects the mode ('e' for encoding or 'd' for decoding).
   - If the mode is 'e', it calls the `Encode()` function with the `private_key` and `Text` (the input message) obtained from their respective input fields.
   - If the mode is 'd', it calls the `Decode()` function with the `private_key` and `Text`.
   - If the mode is neither 'e' nor 'd', it sets the `Result` variable to 'Invalid Mode'.
   - The `Result` variable is then updated with the encoded or decoded result, which is displayed in the corresponding input field.

These functions work together to handle the encoding and decoding operations based on the user's mode selection and input values.

In this program, there is a single key option. The user is prompted to enter a private key, which is used for both encoding and decoding operations. The key is a string that can be of any length, and it is used to perform calculations on the characters of the message for encoding and decoding. The key is applied in a cyclic manner, repeating its characters if the message is longer than the key.

This project was jointly develpoed by me and my team member Sneha Khan. Relevant help was taken from Google while building this application. Some websites that we reffered are Geeks For Geeks, W3 Schools etc. 
