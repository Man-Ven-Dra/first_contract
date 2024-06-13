# NewContract

This is a simple Solidity program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to teach you how to create and deploy a your very first contract.

## Description

This program demonstrates how you can declare different types of variablesi solidity and how to use functions and mapping. The first function named 'mint' lets you mint new tokens to a particular address and the other functions 'burn' lets your burn the token from the address.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., NewContract.sol). Copy and paste the following code into the file:

```pragma solidity 0.8.18;
    contract MyToken {

    // public variables here
   string public tokenName = 'TOKEN';
   string public tokenAbbr = 'TKN';
   uint public totalSupply = 0;
    
    // mapping variable here
   mapping(address => uint) public balances;


    // mint function
   function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
   }
    // burn function
    function burn (address _address, uint _value) public {
      if(balances[_address] >= _value) {
      totalSupply -= _value;
      balances[_address] -= _value;
      }
   }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile NewContract.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, copy a sample address from account tab. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function, paste a the address in the '_address' column and enter amout of tokens you want to mint at this particular address. Finally, click on the "transact" button to execute the function and check the balance and totlal supply to see if the tokens have minted successfully.

## Authors

Manvendra Singh Chauhan
https://www.linkedin.com/in/manvendra-singh-chauhan-975635289/


## License

This project is licensed under the Manvendra License - see the LICENSE.md file for details
