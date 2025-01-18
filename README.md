# **SuprSafe**

**Warning**: This project may have flaws, and caution is advised when using the software. If the program is interrupted during encryption or decryption, there may not be a way to restore the data. SuprSafe has not undergone extensive testing, and its stability and reliability are not guaranteed. Use at your own risk.

**SuprSafe** is a powerful yet user-friendly file encryption software that safeguards your sensitive data using the industry-standard AES-256 algorithm. With its intuitive command-line interface (CLI), SuprSafe empowers you to encrypt and decrypt files effortlessly, ensuring their confidentiality without unnecessary complexity. A companion key generator tool is included to help generate secure main keys.

**Note**: SuprSafe is designed for **one user per distribution**. Each copy of the software can only be used by a single account, ensuring that encryption keys remain secure and isolated for each user.

## Features

- **AES-256 Encryption**: Industry-standard encryption for your files.
- **Secure File Deletion**: Original files are securely deleted after encryption or decryption to ensure no traces are left.
- **Minimal Interface**: Command-line based encryption and decryption, making it lightweight and straightforward.
- **Password Protection:** SuprSafe safeguards your encryption keys with a user-defined password, ensuring an additional layer of security.
- **Key Generator Tool**: A separate utility (`main_key.py`) to generate secure 32-character main keys. Simply run the tool and press Enter to generate new keys, or 'q' to quit. Generated keys are suitable for use with SuprSafe's encryption process.
- **Optional Executable**: SuprSafe can be run as an executable (`SuprSafe.exe`) for easier access, included in the release on GitHub.
- **SuprSafe+ Mode**: An optional security feature that wipes encrypted files after too many failed password attempts.

## Requirements

- **Python 3.x:** Ensure you have Python 3.x installed on your system.
- **Dependency Installation:** Install the necessary dependency using `pip`:

```bash
pip install cryptography
```

## Installation

1. **Clone or Download:** Obtain the SuprSafe codebase by cloning the repository or downloading it directly to your local machine.
2. **Install Dependencies:** Navigate to the SuprSafe directory in your terminal and execute the following command to install the required dependency:

```bash
pip install cryptography
```

## Running SuprSafe

1. **Start the Program:** Launch the software by running the following command in your terminal:

```bash
python main.py
```

Alternatively, you can download the compiled executable (SuprSafe.exe) from the GitHub releases page and run it directly without needing to install Python or dependencies.

## Usage

Once you run the program (either via the Python script or the executable), you will be presented with a simple command-line interface to choose between encryption or decryption. You will be prompted on the initial startup to create an account password. **THIS IS THE PASSWORD THAT WILL BE USED TO ALLOW YOU TO USE THE PROGRAM. MAKE SURE IT IS A COMPLEX PASSWORD**

**Encrypting Files:**

1. Run the SuprSafe executable or Python script from its current location. Alternatively, you can create a shortcut of the executable and place it in a convenient location for easy access.
2. Choose the (e) option to encrypt files - you will be asked to create an account password on first launch. After this, you will be prompted for that password **after** choosing the encrypt/decrypt option in the CLI.
3. Enter the directory path where you want the files to be encrypted.
4. Enter your main key (32-character alphanumeric string). SuprSafe will use this to encrypt the randomly generated AES key and IV.
5. The encrypted files will be saved with extensions like `.enc`, `.enc.tag`, and `.enc.nonce` to indicate their encrypted state.
6. Your files are now encrypted - **DO NOT REMOVE ANY FILES ADDED BY THE SUPRSAFE**.

**Decrypting Files:**

1. Run the SuprSafe executable or Python script from its current location. Alternatively, use a shortcut for easy access.
2. Choose the (d) option to decrypt files.
3. Enter the directory path where the encrypted files are located.
4. Enter the account password created upon first launch.
5. Provide the main key you used during the encryption process.
6. The program will decrypt the selected files and restore them with their original filenames.
7. SuprSafe securely deletes the encrypted files after successful decryption, eliminating any potential data remnants.

## CLI Menu

```text
Welcome to SuprSafe!

Please choose an option:
  (e) Encrypt Files
  (d) Decrypt Files
```

## Security Considerations

**Password Safety:**

- Exercise caution and select a complex and memorable account password. For the main key, ensure you store it off of any digital devices for ultimate security. Losing this password **or** main key will render your encrypted files inaccessible as there's no way to recover them. Consider using password management tools to store your password securely.

**Secure Deletion:**

- SuprSafe prioritizes security by using secure methods to eliminate the original files after encryption or decryption. This guarantees that no traces of sensitive data remain.

**SuprSafe+ Mode:**

- This optional feature enhances security by wiping encrypted files after too many failed password attempts. You can configure this mode during the initial setup or later through the program's interface. SuprSafe+ Mode requires an administrator password, which is separate from your account password. This admin password controls security settings and should be different from your account password to ensure maximum security.

## License

SuprSafe is open-source software licensed under the permissive MIT License. This enables you to freely use, modify, and distribute SuprSafe while complying with the license terms (refer to the LICENSE file for details).
