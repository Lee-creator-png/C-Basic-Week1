# Online Banking System (C)

Console-based banking program written in C for educational use. It supports registering accounts, login, deposits, withdrawals, transfers, password changes, and displays account details. Data persists to `bank_data.txt` in the program directory.

Student Number: 2025554131

## Features
- Register a new account with 6-digit account number
- Login with account number and password
- Deposit funds and withdraw funds with validation
- Transfer funds between accounts
- Change password after verifying current password
- View account details
- Persistent storage in `bank_data.txt`

## Build
Requirements: a C compiler on Windows (e.g., GCC via MinGW or MSVC).

Using GCC (PowerShell):

```
gcc -Wall -O2 -o ONLINEBAKING.exe ONLINEBAKING.C
```

Using MSVC `cl`:

```
cl /EHsc ONLINEBAKING.C /Fe:ONLINEBAKING.exe
```

## Run
From the project directory:

```
./ONLINEBAKING.exe
```

First run creates no data file; you will see:

```
[SYS] No 'bank_data.txt' found. Starting fresh.
```

Non-interactive quick exit (PowerShell):

```
Write-Output "0" | .\ONLINEBAKING.exe
```

## Data File
Path: `bank_data.txt` (same directory). Each line:

```
fullName accountNumber password balance phoneNumber
```

Example:

```
JohnDoe 100001 pass123 100.00 555-1234
```

Note: passwords are stored in plaintext for simplicity; do not use real credentials.

## Usage Notes
- Account number must be unique and 6 digits (100000–999999)
- `fullName` and `phoneNumber` are entered without spaces
- Enter positive numbers for deposit/withdraw/transfer
- Use `0` to exit or logout in menus

## Project Structure
- `ONLINEBAKING.C` — main program source
- `ONLINEBAKING.exe` — compiled executable
- `bank_data.txt` — created at runtime for persistence

## Code Pointers
- File I/O: `loadAccounts` (`c:\Users\RANGALEEANKAWINA\Desktop\ONLINEBAKING\ONLINEBAKING.C:50`) and `saveAccounts` (`c:\Users\NGALEEANKAWINA\Desktop\ONLINEBAKING\ONLINEBAKING.C:76`)
- Menus: `displayPreLoginMenu` (`c:\Users\NGALEEANKAWINA\Desktop\ONLINEBAKING\ONLINEBAKING.C:358`) and `displayLoggedInMenu` (`c:\Users\NGALEEANKAWINA\Desktop\ONLINEBAKING\ONLINEBAKING.C:374`)
- Entry point: `main` (`c:\Users\NGALEEANKAWINA\Desktop\ONLINEBAKING\ONLINEBAKING.C:390`)