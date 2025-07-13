_Offline Password Vault_
Project Overview
The Offline Password Vault is a secure, client-side web application designed to provide a private and self-contained solution for managing your passwords. It operates entirely within your web browser, ensuring that all sensitive password data remains local to your device and never leaves your computer. This project prioritizes user privacy and data security through strong encryption.

**Features**
Offline Operation: No internet connection is required after the initial page load. All data processing and storage occur locally in your browser's localStorage.

AES-256 GCM Encryption: Your passwords are encrypted using the robust AES-256 GCM standard for strong confidentiality and integrity.

PBKDF2 Key Derivation: A high-iteration PBKDF2 algorithm is used to derive the encryption key from your master key, significantly enhancing security against brute-force attacks.

Local Data Storage: Encrypted vault data, including the cryptographic salt and Initialization Vector (IV), are securely persisted in your browser's localStorage.

Intuitive User Interface: A clean, responsive, and easy-to-use interface built with HTML and styled with Tailwind CSS.

**Core Password Management:**

Add, Edit, and Delete password entries.

Copy passwords to clipboard with a single click.

Toggle password visibility for secure viewing.

Password Generation: Generate strong, random passwords directly within the application.

Vault Export: Export your decrypted vault data as a JSON file for backup purposes. (Warning: Handle with extreme care as this file contains plain-text passwords.)

Vault Deletion: Permanently delete all vault data from your browser.

**Technologies Used**
HTML5: For the application's structure.

CSS3 (Tailwind CSS): For modern and responsive styling.

JavaScript (ES6+): For all application logic, including UI interactions and cryptography.

Web Crypto API: Native browser API for secure cryptographic operations.

**Setup and Running the Project**
Since this is a static web application, deployment is very straightforward.

Method 1: Local Setup (Simplest)
Download/Save Files:

Ensure you have index.html (the main application file) and style.css (the custom CSS) in the same directory.

Open in Browser: Simply double-click the index.html file. It will open in your default web browser.

**Usage**
Set Up Vault: On first use, create a strong master key. This key is critical and cannot be recovered if lost.

Unlock Vault: Enter your master key to access your encrypted passwords.

Manage Entries: Use the "Add New Entry" button to add credentials. You can edit, delete, copy, and toggle visibility of existing entries. Use the "Generate Password" button for strong random passwords.

Export/Delete: Use "Export Vault" for backups (handle the exported file with extreme care!) and "Delete Vault" to permanently remove data from your browser.

**Security Considerations**
Master Key: The entire security of your vault relies on your master key. Choose a long, complex, and unique one.

Offline Data: Your data is stored locally. While this enhances privacy, if your device is compromised, your localStorage could be vulnerable if your master key is weak or exposed.

Exported JSON: The exported password_vault_export.json file contains plain-text passwords. Secure it immediately and appropriately.

Browser Security: Keep your web browser updated to ensure you have the latest security features and Web Crypto API implementations.

