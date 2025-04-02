# Decentralized Image Upload and Sharing

This project facilitates decentralized image upload and sharing on the blockchain using Solidity for the smart contract and React for the front-end interface. It enables users to securely upload images to IPFS (InterPlanetary File System) and share access with specified users through smart contract functionality.


## Features
- **Decentralized Storage:** Images are uploaded to IPFS, ensuring decentralized and immutable storage.
- **Smart Contract:** Utilizes Solidity smart contracts on the Ethereum blockchain for access control and ownership management.
- **Access Control:** Users can grant or revoke access to their uploaded images to specific individuals through the smart contract.

## Technologies Used
- **Solidity:** Smart contract development for ownership and access control.
- **React:** Front-end interface for uploading images and managing access.
- **IPFS:** Decentralized storage protocol for hosting uploaded images.

## Installation & Setup

### Backend (Hardhat & Smart Contract)
1. Clone the repository:
    ```bash
    git clone https://github.com/chinu2003/file-storage.git
    ```
2. Navigate to the project directory:
    ```bash
    cd file-storage
    ```
3. Install dependencies:
    ```bash
    npm install
    ```
4. Compile the smart contract:
    ```bash
    npx hardhat compile
    ```
5. Deploy the smart contract to an Ethereum testnet or local development environment:
    ```bash
    npx hardhat run scripts/deploy.js --network <network-name>
    ```

### Frontend (React Application)
1. Navigate to the React client directory:
    ```bash
    cd client
    ```
2. Install dependencies:
    ```bash
    npm install
    ```
3. Start the React application:
    ```bash
    npm start
    ```

## Configuration
1. Set up environment variables:
    - Obtain API keys from Pinata to interact with IPFS.
    - Update the React component (`FileUpload.js`) with your Pinata API keys.
2. Update the smart contract address in `App.js` after deployment.

## Usage Instructions
1. **Install Metamask:**
    - Ensure Metamask is installed and configured in your browser for Ethereum interactions.
2. **Update Contract Address:**
    - After smart contract deployment, update the contract address in `App.js` within the React application.
3. **Uploading Images:**
    - Use the upload functionality to store images on IPFS.
4. **Accessing Uploaded Images:**
    - Click "Get Data" after uploading an image on Pinata.
    - If an image is not uploaded, it will throw an error: "You don't have access".
5. **Accessing Other Users' Images:**
    - Enter the user's Ethereum address in the designated box and click "Get Data".
    - Access is granted only if the user has shared their image with you via the smart contract.
    - Otherwise, it will throw an error: "You don't have access".

Following these steps ensures a seamless experience with decentralized image storage and sharing while maintaining secure access control.
