# Error
This Solidity smart contract named Error demonstrates the usage of three different types of error-handling mechanism in Solidty which are require(), revert(), and assert() statements.
# Descriptions
The contract has three different functions; the first function uses the require() statements to validate the input _i - it checks whether _i is less than 100. The second function uses the revert() statements to revert state changes if a specific condition is unmet. The third function is assert() accounts that check for internal errors. It asserts the state variable 'num' must be 0. If 'num' is not 0, the assert statement will fail, and the transaction will be reverted, consuming all the gas.
# Getting Started
#Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Error.sol). Copy and paste the following code into the file:
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.17;

contract Error {
    uint256 public num;

    // Using require() to validate conditions.
    function checkRequire(uint256 _i) public {
        require(_i < 100, "Value must be less than 100");
        num = _i;
    }

    // Using revert() to revert state changes.
    function checkRevert(uint256 _i) public {
        if (_i <= 10) {
            revert("Input must be greater than 10");
        }
        num = _i;
    }

    // Using assert() to check for internal errors.
    function checkAssert() public view {
        assert(num == 0);
    }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

# Author
[@4Farrx](https://twitter.com/4Farrx)

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
