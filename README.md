# Solidity Contract

This Solidity program demonstrates the creation of a basic ERC20-like token contract with minting and burning functionalities. The purpose of this project is to familiarize blockchain developers with the basics of creating and managing a token on the Ethereum blockchain.
## Description

This Solidity contract defines a simple token with the following features:
- The creation of public variables to store details about the token (Token Name, Token Abbreviation, Total Supply)
- A mapping of address to balance
- A mint function to create new tokens and assign them to a specific address
- A burn function to destroy tokens from a specific address.

## Getting Started

### Installing

To get started with this project, you will need to have a Solidity development environment set up. We recommend using Remix, an online Solidity IDE. Follow these steps to install and prepare your environment:

1. **Go to Remix:** Visit the Remix IDE at [Remix](https://remix.ethereum.org/).
2. **Create a new file:** Click on the "+" icon in the left-hand sidebar to create a new file. Save the file with a `.sol` extension (e.g., `MyToken.sol`).
3. **Copy and paste the template code:** If a template code is provided, Copy the code provided and paste it into your new file.

### Executing program

To run this program, use Remix as follows:

1. **Copy the following code into your file:**

```javascript

pragma solidity 0.8.26;

contract MyToken {
    string public tokenName = "POGO";
    string public tokenAbbrv = "PGO";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }

}

```

2. **Compile the code:** Click on the "Solidity Compiler" tab in the left-hand sidebar. Ensure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile MyToken.sol" button.

3. **Deploy the contract:** Click on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

4. **Interact with the contract:** Once deployed, interact with the contract by calling the `mint` and `burn` functions to manage token balances.

## Authors

VincyDaniel 
[VincyDaniel](https://www.linkedin.com/in/vince-daniel-del-rosario-815a11205/)

## License

This project is licensed under the VincyDaniel License - see the LICENSE.md file for details
