# **ERC20 and Vault Contracts README**

## **Overview**
This repository contains the implementation of two essential smart contracts: 

1. **ERC20 Token Contract**  
   - A standard implementation of the ERC20 token as defined by the Ethereum Improvement Proposal (EIP-20).  
   - It supports basic token operations like minting, transferring, and querying balances.

2. **Vault Contract**  
   - A secure vault for managing and interacting with ERC20 tokens.  
   - It allows deposits, withdrawals, and tracks balances while ensuring only authorized operations.

---

## **Contracts Overview**

### **1. ERC20 Token Contract**
The ERC20 contract defines a fungible token standard. It provides:
- **Compliance with EIP-20:** Implements all required functions like `totalSupply`, `transfer`, and `balanceOf`.
- **Minting and Burning (Optional):** Includes functionality to mint new tokens or burn existing ones.
- **Event Logging:** Emits events such as `Transfer` and `Approval` for on-chain monitoring.
- **Customizable Details:**
  - **Token Name:** Easily set the name of your token.
  - **Symbol:** Define a ticker symbol.
  - **Decimals:** Specify the number of decimal places for token divisibility.

#### Key Functions:
- `transfer(address to, uint256 value)` – Transfers tokens to another address.
- `approve(address spender, uint256 value)` – Approves another address to spend tokens on behalf of the caller.
- `transferFrom(address from, address to, uint256 value)` – Transfers tokens from one address to another, using the allowance mechanism.
- `mint(address to, uint256 value)` – Mints new tokens to the specified address.
- `burn(uint256 value)` – Burns tokens from the caller's account.

---

### **2. Vault Contract**
The Vault contract acts as a secure escrow for ERC20 tokens, enabling users to deposit and withdraw tokens with ease.

#### Features:
- **Deposit Functionality:** Users can safely deposit tokens into the vault.
- **Withdrawals:** Users can withdraw their tokens at any time.
- **Balance Tracking:** The vault maintains individual user balances.
- **Access Control:** Restricts unauthorized access to admin-specific functionalities.
- **Event Logging:** Emits events for deposit and withdrawal activities for transparency.

#### Key Functions:
- `deposit(uint256 amount)` – Deposits a specified number of tokens into the vault.
- `withdraw(uint256 amount)` – Withdraws tokens from the user's vault balance.
- `getBalance(address account)` – Returns the token balance of a specific user.
- `setTokenAddress(address token)` – (Admin only) Links an ERC20 token to the vault.

---

## **How to Use**

### **Prerequisites**
- Install **Node.js** and **npm**.
- Install **Hardhat** for local Ethereum development.
- Have a wallet like **MetaMask** for testing purposes.
- Deploy the ERC20 contract before deploying the Vault contract.

## **Security Considerations**
1. **Access Control:** Ensure only authorized addresses can mint tokens or set the token address in the Vault.
2. **Reentrancy Guard:** Prevent reentrancy attacks in deposit and withdrawal functions.
3. **Proper Approvals:** Users must approve the vault before depositing tokens.

---

## **License**
This project is licensed under the **MIT License**. Feel free to use, modify, and distribute this software.

---

## **Contact**
For questions or feedback, please contact:
- **Email:** yashwanths.sd@gmail.com
- **GitHub Issues:** [Open an Issue](https://github.com/your-repo/erc20-vault-contracts/issues)

Enjoy seamless token management with our ERC20 and Vault contracts! 🎉
