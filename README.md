[README.md](https://github.com/user-attachments/files/34754539/README.md)[main.py](https://github.com/user-attachments/files/34670175/main.py)
Beatrice Affram Dantaa
10358088

Text Encryption and Decryption

A simple Python program that hides a message by shifting each letter forward in the alphabet (the Caesar cipher), then turns it back again.

How to run
bash
python main.py

Type your message and a shift number when asked.

Example
Enter your message: Hello
Enter shift number: 3

Encrypted message: Khoor
Decrypted message: Hello
Notes
Only letters are changed. Numbers, spaces and symbols stay the same.
The shift must be a whole number.
This is for learning, not for protecting real secrets.oading README.md…]()

[INFORMATION SYSTEMS SECURITY VULNERABILITY ASSESSMENT AND IT RISK ANALYSIS ON UPSA.docx](https://github.com/user-attachments/files/34670164/INFORMATION.SYSTEMS.SECURITY.VULNERABILITY.ASSESSMENT.AND.IT.RISK.ANALYSIS.ON.UPSA.docx)
# Report-Analysis-and-Crptography
Reporting on security systems and converting plaintext to ciphertext

def encrypt(text, shift):
    encrypted_text = ""

    for char in text:
        if char.isalpha():
            start = ord('A') if char.isupper() else ord('a')

            new_char = chr((ord(char) - start + shift) % 26 + start)

            encrypted_text += new_char
        else:
            encrypted_text += char

    return encrypted_text


def decrypt(text, shift):
    return encrypt(text, -shift)


print("===== TEXT ENCRYPTION AND DECRYPTION SYSTEM =====")

message = input("Enter your message: ")

shift = int(input("Enter shift number: "))

encrypted = encrypt(message, shift)

print("\nEncrypted message:", encrypted)

decrypted = decrypt(encrypted, shift)

print("Decrypted message:", decrypted)
