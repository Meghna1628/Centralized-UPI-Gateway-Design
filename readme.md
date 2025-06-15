# Centralized UPI Payment Gateway

## Overview

This project simulates a **Centralized UPI Payment Gateway** with strong security mechanisms to ensure secure and verifiable digital transactions. It integrates:

- **Blockchain** for immutable transaction logging,
- **Lightweight Cryptography (LWC)** using the SPECK algorithm for fast encryption in resource-constrained devices,
- **Quantum Cryptography simulation** (Shor’s Algorithm) to demonstrate vulnerabilities in traditional cryptographic methods.

The system is built using three separate devices:
- **User Laptop**: Initiates payment by scanning a QR code and entering transaction details.
- **Merchant's UPI Machine**: Encrypts Merchant ID and communicates with the bank and user.
- **Bank Laptop**: Maintains transaction history, verifies credentials, and updates balances.

## Key Features

- Encrypted QR-based UPI transactions using AES algorithm
- Blockchain ledger for storing validated payments
- SPECK algorithm for LWC
- Quantum Cryptography attack simulation
- Simulated inter-device communication via socket programming

## Installation
Install the required libraries using the following command:
```bash
pip install pycryptodome pillow qrcode
```
## Usage

#### Step 1: Configure IPs
Edit config.json to match the device IP addresses:
```bash
BANK_SERVER_IP: "127.0.0.1"
BANK_SERVER_PORT: 12345
UPI_SERVER_IP: "127.0.0.1"
UPI_SERVER_PORT: 5050
```
#### Step 2: Run All Components
```bash
python Bank.py
python User_Laptop.py
python UPI_Machine.py
python speck_algo.py
python aes_encryption.py
```
## Steps for Transaction
1. Register both user and merchant in Bank to generate both MMID, and MID by providing necessary details in input fields.
2. Now, users can proceed with transactions. Merchant enters his MID to generate a QR Code
3. Users scan this QR code and enters transaction details. 
4. First, merchant clicks "Ready to Receive" button on UPI Machine to receive details from user. Then user clicks "Send & Pay via UPI" button on user laptop to send the transaction details.
5. UPI Machine forwards the received transaction details to the Bank and displays a success/failure message.
6. Bank validates and logs the transaction using a blockchain ledger.

## Team Members

| Name                    | ID             |
|-------------------------|----------------|
| Meghna Reddy Yadma      | 2021A3PS2762H  |
| Rishit Polepeddi        | 2022AAPS0311H  |
| Shashwat Pandey         | 2022A7PS1299H  |
| Nachiket Kale           | 2021AAPS2880H  |
| Sai Sushruth Pothireddy | 2021AAPS1680H  |

