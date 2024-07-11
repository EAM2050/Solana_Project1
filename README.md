# Solana Devnet Dapp

## Introduction

This project is a simple React application demonstrating how to interact with the Solana blockchain using the Phantom Wallet. The app allows users to create a new Solana account, connect their Phantom Wallet, transfer SOL between the created account and the connected Phantom Wallet, and disconnect the wallet.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Node.js and npm installed on your machine.
- Phantom Wallet extension installed in your browser.

## Getting Started

Follow these instructions to set up your development environment and run the application.

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/your-repo/solana-wallet-integration.git
   cd solana-wallet-integration
   ```

2. **Install dependencies:**

   ```sh
   npm install
   ```

### Running the Application

1. **Start the development server:**

   ```sh
   npm start
   ```

2. **Open your browser and navigate to:**

   ```sh
   http://localhost:3000
   ```

## Application Features

### Create a New Solana Account

Click the "Create a New Solana Account" button to generate a new Solana account and airdrop 2 SOL into it.

### Connect to Phantom Wallet

Click the "Connect to Phantom Wallet" button to connect your Phantom Wallet. If the connection is successful, the wallet's public key will be displayed.

### Transfer SOL to Phantom Wallet

After connecting your Phantom Wallet and creating a new Solana account, click the "Transfer SOL to Phantom Wallet" button to transfer 1 SOL from the created account to your connected Phantom Wallet.

### Disconnect from Wallet

Click the "Disconnect from Wallet" button to disconnect your Phantom Wallet.

## Code Explanation

### Imports

The application imports necessary functionalities from `@solana/web3.js` and React. It also fixes the polyfill issue with the buffer by importing `buffer` and setting `window.Buffer`.

### Types and Interfaces

Defines types and interfaces for Phantom events, request methods, and the Phantom provider.

### getProvider Function

This function checks if the Phantom provider is available in the window object and returns it.

### React Component: `App`

- **State Variables:** 
  - `provider`: Stores the Phantom provider.
  - `receiverPublicKey`: Stores the public key of the connected Phantom Wallet.
  - `senderKeypair`: Stores the keypair of the created Solana account.
  - `connection`: Establishes a connection to the Solana devnet.

- **useEffect:** 
  - Initializes the Phantom provider when the component mounts.

- **createSender Function:** 
  - Generates a new keypair and requests an airdrop of 2 SOL into the created account.

- **connectWallet Function:** 
  - Prompts the user to connect their Phantom Wallet and stores the wallet's public key.

- **disconnectWallet Function:** 
  - Disconnects the connected Phantom Wallet and clears the public key.

- **transferSol Function:** 
  - Transfers 1 SOL from the created account to the connected Phantom Wallet.

- **Render Method:** 
  - Displays buttons for creating an account, connecting/disconnecting the wallet, and transferring SOL based on the state.

## Deployment

To deploy the application, you can use any static site hosting service such as Vercel, Netlify, or GitHub Pages.

## Contributing

If you want to contribute to this project, please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.
