## ERC 20 Token with Foundry

Foundry is the new kid in town for smart contract developement and testing, it's fast and the tests are written in solidity.
for more info check [foundry](https://onbjerg.github.io/foundry-book/).

This are the getters, functions and events that is defined in ERC-20 Token standard

```solidity
pragma solidity ^0.8.0;

interface IERC20 {

    function totalSupply() external view returns (uint256);
    function balanceOf(address account) external view returns (uint256);
    function allowance(address owner, address spender) external view returns (uint256);
   
    function transfer(address recipient, uint256 amount) external returns (bool);
    function approve(address spender, uint256 amount) external returns (bool);
    function transferFrom(address sender, address recipient, uint256 amount) external returns (bool);

    event Transfer(address indexed from, address indexed to, uint256 value);
    event Approval(address indexed owner, address indexed spender, uint256 value);
}
```