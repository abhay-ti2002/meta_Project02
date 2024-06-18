Create a Token
Simple Overview of Use/Purpose
This project demonstrates how to create a simple token on the Ethereum blockchain using Solidity. It covers fundamental concepts such as storing token details, minting new tokens, and burning existing tokens.

Description
You will develop a smart contract named MyToken using Solidity 0.8.18. This contract will include public variables for token details, a mapping for balances, a mint function to increase the supply, and a burn function to decrease it, ensuring sufficient balance before burning.

Getting Started
Installing
Visit the Remix IDE.
No installations are required as Remix is an online IDE.
Executing Program
Open Remix IDE.
Create a new file named MyToken.sol.
Copy and paste the following code into the file:
// SPDX-License-Identifier: MIT
pragma solidity >=0.6.12 <0.9.0;

contract MyToken {
    // public variables here
    string public tokenName = "Abhay Tiwari";
    string public tokenAbbrv = "Abhy";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address tokenaddress, uint value) public {
        totalSupply += value;
        balances[tokenaddress] += value;
    }

    // burn function
    function burn(address tokenaddress, uint value) public {
        if (balances[tokenaddress] >= value) {
            totalSupply -= value;
            balances[tokenaddress] -= value;
        }
    }
}
Compile the contract by clicking on the "Solidity Compiler" tab and then "Compile MyToken.sol".
Deploy the contract by navigating to the "Deploy & Run Transactions" tab, selecting your contract, and clicking "Deploy".
Interact with your deployed contract using the provided interface to call functions like tokenName, tokenAbbr, totalSupply, mint, and burn.
Help
For common problems or issues:

Ensure you have a stable internet connection while using Remix IDE.
Make sure the Solidity version in Remix is set to 0.8.18.
If you encounter any errors during compilation or deployment, double-check the syntax and version compatibility.
For further assistance, you can refer to the Remix documentation or run the help command within Remix IDE if available.

Authors
Contributors:

GitHub:https://github.com/abhay-ti2002
LinkedIn: https://www.linkedin.com/in/abhay-tiwari-974501249/
License
This project is licensed under the MIT License - see the LICENSE.md file for details.
