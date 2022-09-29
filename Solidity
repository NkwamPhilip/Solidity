// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

contract ageEth {

    struct transact {
        address addr;
        uint256 curr;
    }
    transact[] public people;
    mapping(address => uint256) public addressBal;

    uint256 internal balance = 0;

    function buyToken(address _addr, uint256 currUSD) public {
        uint256 curr2eth = currUSD/1347;
        balance += curr2eth;
        people.push(transact(_addr, curr2eth));
        addressBal[_addr] = balance;

    }

    function sellToken(address _addr, uint256 newUSD) public {
        uint256 curr2eth = newUSD/1347;
        balance -= curr2eth;
        people.push(transact(_addr, balance));
        addressBal[_addr] = balance;
    }

}

