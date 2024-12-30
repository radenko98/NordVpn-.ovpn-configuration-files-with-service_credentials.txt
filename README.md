# NordVPN Configuration Files (Updated)

This repository contains updated NordVPN configuration files, downloaded and modified on **December 30, 2024**. 

## Folder Structure
- **UDP**: Contains approximately 6,730 configuration files.
- **TCP**: Contains approximately 6,730 configuration files.
- All configuration files were downloaded directly from the official [NordVPN website](https://nordvpn.com).

## Modifications Made
1. **Removed `ping-timer-rem` Directive**  
   - The `ping-timer-rem` directive was an obsolete feature used in older OpenVPN versions to manage ping timers in "remotely" initiated mode.  
   - In OpenVPN 2.x and newer versions, this directive is deprecated and unnecessary.  
   - Its presence in the original NordVPN `.ovpn` files caused compatibility issues with newer OpenVPN clients, rendering the configuration files non-functional.  
   - As a result, this directive was removed to ensure the `.ovpn` files work seamlessly with modern OpenVPN clients.

2. **Added `service_credentials.txt` to `auth-user-pass` Directive**  
   - The line `auth-user-pass` was modified to include `service_credentials.txt`.  
   - This change eliminates the need to manually enter your username and password each time you use a configuration file.  
   - Ensure that the `service_credentials.txt` file contains your NordVPN credentials in the following format:
     ```
     username
     password
     ```

## How to use!
Download **TCP, UDP** and **Service Credentials Update** rar files from https://drive.google.com/drive/folders/1FcoJz53FHTtUgddxWKhykcXmGXdRHV8W?usp=sharing
(password:windows)
1. Extract **TCP** and **UPD** config files to **C:\Program Files\OpenVPN Connect\Config**, if config folder does not exist, create it yourself.
2. Extract **Service Credentials Update** to **C:\Program Files\OpenVPN Connect\Config**
3. Run Update_ServiceCredentials.exe file
3.1. Select parent directory that contains all subdirectories (for example: C:\Program Files\OpenVPN Connect\Config\TCP)
   <img width="960" alt="image" src="https://github.com/user-attachments/assets/d86e9a67-bf5e-46f5-9a63-2666c18127ea" />
3.2. Enter your username in line #1 and your password in line #2
   <img width="737" alt="image" src="https://github.com/user-attachments/assets/af8f98b4-f90b-4c42-b306-a40203c283d8" />
4. Update_ServiceCredentials.exe will scans all subdirectories within the chosen directory Updates the first and second line with your input.
5. Run .ovpn config files!

## You can find your username and password here: 
https://my.nordaccount.com/dashboard/nordvpn/manual-configuration/service-credentials/ 

<img width="1142" alt="image" src="https://github.com/user-attachments/assets/a60b1750-87d6-40fc-a770-bb58885bda99" />



## Why These Changes Were Made
- **Compatibility**: The removal of `ping-timer-rem` ensures compatibility with modern OpenVPN clients.
- **Convenience**: Adding `service_credentials.txt` simplifies the user experience by automating credential entry.

## Usage
1. Place your `service_credentials.txt` file in the same directory as your `.ovpn` configuration files.
2. Use any OpenVPN client to import the `.ovpn` files and connect to NordVPN servers or simply open .ovpn configuration file.
