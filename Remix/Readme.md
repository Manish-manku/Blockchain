Using a Development Environment such as Remix to compile and deploy your smart contract.
Navigate to remix and select contracts > 1_Storage.sol from the File Explorers pane.
Create or Modify the existing smart contract:
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.17;

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.0.0/contracts/token/ERC20/ERC20.sol";

    contract MyToken is ERC20 {
        constructor(string memory name, string memory symbol) ERC20(name, symbol) {
            // Mint 100 tokens to msg.sender
            // 1 token = 1 * (10 ** decimals)
            _mint(msg.sender, 100 * 10 ** uint(decimals()));
        }
    }
Note: You can look more into it from Solidity docs and Solidity by Example
Compile using Solidity Compiler(left nav pane):
Check that your compiler version is same as the versions specified in the pragma solidity statement(0.8.17)
Deploy the Contract:
1. Click the Deploy and Run Transactions Icon on the left side menu.
2. Choose Injected Web3 as your environment.
3. Connect MetaMask to GoerliTest net.
4. Click Deploy and select Confirm in the MetaMask notification window to pay for the transaction.
View Contract Details:
Copy the contract address from the Deployed Contracts window on the left panel & head to Etherscan explore the details of your deployed smart contract1_Storage.sol
