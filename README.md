
# Wi-Fi Profile Password Retriever

This Python script retrieves and displays the Wi-Fi profiles stored on a Windows machine, along with their corresponding passwords (if available).

## Features

- List all saved Wi-Fi profiles on the system.
- Retrieve the password of each profile (if the password is stored).
- Display the results in a formatted table.
- Handle cases where the password is not available.

## Requirements

- **Operating System:** Windows
- **Python:** 3.x or higher
- **Permissions:** Administrator privileges are required to access the Wi-Fi profile details and passwords.
  
## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/wifi-profile-password-retriever.git
   ```

2. Navigate to the project directory:
   ```bash
   cd wifi-profile-password-retriever
   ```

3. No additional dependencies are required for this script. It relies on Python's built-in `subprocess` module.

## Usage

1. Open a terminal or command prompt with Administrator privileges.
2. Run the script:
   ```bash
   python wifi_password_retriever.py
   ```
   The script will display all saved Wi-Fi profiles and their corresponding passwords (if available) in a tabular format.

   Example output:
   ```plaintext
   Profile Name                  | Password
   --------------------------------|--------------------------------
   HomeNetwork                   | mypassword123
   OfficeWiFi                    | 
   ```

   - If the profile doesn't have a stored password, it will display an empty value.

## How It Works

1. The script first retrieves a list of all Wi-Fi profiles stored on the system using the `netsh wlan show profiles` command.
2. For each profile, it checks for the presence of a stored password by using the `netsh wlan show profile <profile_name> key=clear` command.
3. The output is parsed, and the profile name and password (if available) are displayed in a neatly formatted table.

## Notes

- This script only works on Windows.
- The script requires Administrator access to retrieve the passwords for Wi-Fi profiles.
- It is recommended to run this script on your own machine or with explicit permission from the system owner.
---

This README provides an overview of the program, its usage, installation instructions, and requirements.
