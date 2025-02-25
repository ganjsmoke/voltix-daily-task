# Auto Daily Task Claim for Voltix

This script automates the process of claiming daily tasks from the Voltix platform using Solana wallet private keys. It signs in with the user's private keys, checks for available tasks, verifies them, and attempts to claim them periodically.
Register : https://voltix.ai/login?ref=OPBK1

## Installation

### Prerequisites
- **Node.js**: This script requires Node.js 14.x or above.
- **Solana Wallet**: A Solana wallet private key (Base58) is required.
- **Voltix Account**: You need a registered account on Voltix.

### Install Dependencies
Clone the repository and install dependencies:

```bash
git clone https://github.com/ganjsmoke/voltix-daily-task.git
cd voltix-daily-task
npm install
```

### Setup Private Keys
Before running the script, create a file named private_keys.txt in the root directory to store your Solana wallet private keys (Base58 encoded). Each key should be on a new line:

```
your_private_key_1
your_private_key_2
```

### Run the Bot

```bash
node index.js
```

### What the script does:
1. Authentication: The script signs into Voltix using the Solana private key and retrieves an authentication token.
2. Fetch Tasks: It retrieves daily unclaimed tasks from Voltix.
3. Verify Tasks: Each task is verified before being claimed.
4. Claim Tasks: The script then claims the tasks.
5. Repeat: The process will automatically repeat every 12 hours (default).
