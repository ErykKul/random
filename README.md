# random

![image](https://github.com/user-attachments/assets/6d9b80c4-6cef-499a-95bb-a2f65d94138e)

This project is a simple HTML form around the [isaacCSPRNG](https://github.com/macmcmeans/isaacCSPRNG), here used for the generation of a string of random 7-bit ASCII graphemes.

The form can be used as a POC of a password management tool. The idea behind it is that you can use the same passphrase to generate passwords for different accounts. For example, you can use the URL of the website for which you are generating the password as the first part of the seed (plain text) and your passphrase as the second part. Your passphrase (or its hash) is not stored anywhere, it is not sent anywhere, and you do not need an online account to store the generated passwords. The passwords are not stored but are re-generated each time you click the generate button using the plain text and secret parts of the seed as the seed for the ISAAC CSPRNG. After clicking the generate button, the generated password is copied to the clipboard and can be used by pasting it in the login form. The password is a string of random 7-bit ASCII graphemes (``` ~`_-+={}[]<>/,.:;?|!@#$%^&*()0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz```) and should fit most of the password requirements. By default, the generated password length is 21 characters (or ```42/2```), which can be also changed in the form.

Use at your own risk and preferably only as a proof-of-concept, or at least in a two-factor authentication context. You can access the form at: [todo](todo)

This project is minimalistic on purpose such that the code is easy to review before using (it is advised to at least take a look at it before even considering it).
