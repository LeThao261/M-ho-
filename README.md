# M-ho-
Mã hoá theo thuật toán Ceasar
def caesar_cipher(text, shift, alphabet):
    encrypted_text = ""
    for char in text.upper():
        if char in alphabet:
            new_index = (alphabet.index(char) + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
        else:
            encrypted_text += char  # Giữ nguyên khoảng trắng hoặc ký tự đặc biệt
    return encrypted_text

alphabet_23 = "ABCDEGHIJKLMNOPQRSTUVWXYZ"

# Tên cần mã hóa
text = "LE PHUONG THAO"

# Mã hóa với Key 26 
encoded_text = caesar_cipher(text, 3, alphabet_23)

print("Mã hóa:", encoded_text)

