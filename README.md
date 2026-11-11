[main.py](https://github.com/user-attachments/files/34670175/main.py)
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
