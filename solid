// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    string public tokenName;
    string public tokenAbbrv;
    uint public totalSupply;
    mapping(address => uint) public balances;

    constructor(string memory _tokenName, string memory _tokenAbbrv, uint _totalSupply) {
        tokenName = _tokenName;
        tokenAbbrv = _tokenAbbrv;
        totalSupply = _totalSupply;
        balances[msg.sender] = _totalSupply;
    }

    function mint(address account, uint value) public {
        totalSupply += value;
        balances[account] += value;
    }

    function burn(address account, uint value) public {
        require(balances[account] >= value, "Insufficient balance");
        totalSupply -= value;
        balances[account] -= value;
    }
}
