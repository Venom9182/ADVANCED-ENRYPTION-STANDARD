# AES Encryption Messenger

This Java project implements AES (Advanced Encryption Standard) encryption with GCM (Galois/Counter Mode) to securely encrypt and decrypt messages. It uses a dynamically generated AES key and ensures both confidentiality and integrity of the encrypted messages.

## Description

AES Encryption Messenger is a simple encryption utility that demonstrates how to use the AES algorithm in GCM mode with Java's `javax.crypto` package. The project generates a secret key, encrypts a given message using AES, and then allows the message to be decrypted back to its original form. The encryption is done using AES with a 128-bit key size, and the encrypted data is encoded using Base64 for easier transmission and storage.

This project is useful as an introduction to modern encryption techniques in Java and can be expanded for applications requiring secure messaging, data protection, or encryption/decryption services.

### Key Features:
- **AES with GCM Mode**: Uses AES/GCM/NoPadding for secure encryption.
- **Dynamic Key Generation**: Automatically generates a random AES secret key.
- **Base64 Encoding**: Encrypted data is encoded in Base64 format for ease of use.
- **Message Encryption and Decryption**: Can encrypt and decrypt any plain text messages using the generated key.

### AES Encryption Overview:
- **AES**: A symmetric encryption algorithm widely used for securing data.
- **GCM Mode**: Provides both encryption and authentication, ensuring message integrity and confidentiality.
- **No Padding**: GCM mode does not require padding as it operates on blocks of data.

## How It Works

1. **Initialization**: The AES secret key is dynamically generated when the encryption process starts.
2. **Encryption**: A plain text message is encrypted using the AES secret key and the GCM cipher mode. The encrypted data is encoded into Base64 format.
3. **Decryption**: The encrypted message is decoded from Base64, and the AES key is used with the GCM cipher to decrypt it back to the original plain text.

## Installation and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/aes-encryption-messenger.git
   cd aes-encryption-messenger
2. **Compile and Run the Project: Ensure you have JDK 8 or higher installed on your system.**
    javac AES.java
    java AES

3.** Example Code: The following code snippet shows how to use the AES class to encrypt and decrypt a message:**
AES aes = new AES();
aes.init(); // Initialize the AES key
String encryptedMessage = aes.encrypt("Hello, World!"); // Encrypt the message
String decryptedMessage = aes.decrypt(encryptedMessage); // Decrypt the message

System.out.println("Encrypted Message: " + encryptedMessage);
System.out.println("Decrypted Message: " + decryptedMessage);

**4. Output: When you run the program, you should see an encrypted message (in Base64) and the decrypted message, which matches the original input.
**



