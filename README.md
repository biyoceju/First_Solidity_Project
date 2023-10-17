# My first Token

The purpose of this program is to create a token called CELIO, abbreviated CEY and with an initial total supply of 2000 ceys. It is the first project, I wrote in solidity after following the course entitled 'Getting Started in Solidity' on metacrafters.io.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The program has 2 functions:  a minting function (to mint new cey tokens and increase its total supply) and a burning function (to burn cey tokens and decrease its total supply). For the burn function, the account balance of the user should be greater than or equal to the amount he wants to burn. If this requirement is not fulfilled, the account balance and the total supply won't change.This program can be used to construct more complex projects in the future. 


## Getting Started

### Installing

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ceytoken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract together {

    // public variables here

string public Token_Name= "CELYO";
string public Token_Abbrv= "CEY";
uint public Total_Supply= 2000;


    // mapping variable here

mapping(address => uint) public balances;

    // mint function

function mint(address payable Addr1, uint Amt1) public returns (uint, uint){
  return  (Total_Supply += Amt1, balances[Addr1] += Amt1);
}
    // burn function

function burn(address Addr2, uint Amt2) public  returns (uint, uint) {
    if (balances[Addr2] >= Amt2){
        return (Total_Supply -= Amt2, balances[Addr2]-= Amt2);
    } else {
        return (Total_Supply, balances[Addr2]);
    }
    
}
}

### Executing program
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.20" (or another compatible version), and then click on the "Compile ceytoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "TOGETHER" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function and the burn function. Click on the "TOGETHER" contract in the left-hand sidebar, and then click on the arrow near "mint" or  "burn" functions. Enter the address and the amount you would like to mint or burn. Finally, click on the "transact" button to execute the function and retrieve the balance and the total supply by clicking repectively on the balance button and on the Total_Supply button. 


## Author
Metacrafter Celestin
@BiakeJunior [https://twitter.com/BiakeJunior]

## License
This project is licensed under the MIT License - see the LICENSE.md file for details 
