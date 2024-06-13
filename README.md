# SolidityProject2

This Solidity program is a simple Token creation program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a contract written in Solidity, which is a programming language used for developing smart contracts on the Ethereum blockchain. The contract has public variables associated with the token like token aame,token abbreviation and total supply of token. A mint function updates increases the total supply by that number and increases the balance of the “sender” address by that amount. A burn function that works the opposite of the mint function, as it destroys tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., TokenCreation.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.7;

contract MyToken {

    // public variables here
    string public tokenName= "apple";
    string public tokenAbbrev = "APL" ;
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint ) public balances;

    // mint function
    function mint(address _address , uint _value) public {
        totalSupply+= _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address , uint _value) public {
        if(balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
        

    }

}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.7" (or another compatible version), and then click on the "Compile TokenCreation.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn functions. 

## Authors

Arundhati Singh
