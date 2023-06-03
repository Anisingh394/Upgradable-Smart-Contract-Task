# Upgradable-Smart-Contract-Task
Creating an upgradable smart contract with the Transparent Proxy Pattern and Gnosis Multisignature wallet involves multiple phases of development. Each phase introduces new features and enhancements to the contract while maintaining compatibility with the previous versions. Below is an outline of the tasks for each phase:

Phase 1 - Contract Version 1:
- Create a simple ERC20 contract with a pre-minting of 1 million tokens.
- Implement basic token functionalities such as transfer, balanceOf, and approve.
- Deploy the initial version of the contract.

Phase 2 - Contract Version 2:
- Add the functionality to mint and burn tokens.
- Implement the allowance mechanism with functions like transferFrom and increase/decreaseAllowance.
- Use the call method for all payable and transaction functions to make them compatible with the Transparent Proxy Pattern.
- Deploy the updated version of the contract, ensuring compatibility with the previous version.

Phase 3 - Contract Version 3:
- Add a Reentrancy Guard to protect vulnerable functions from reentrancy attacks. This can be achieved by creating a custom modifier that implements the necessary checks.
- Add the onlyOwner modifier wherever necessary to restrict access to specific functions to only the contract owner. Implement this as a custom modifier as well.
- Perform thorough testing of all the functionalities introduced in Phase 3, ensuring that the contract remains compatible with the previous versions.
- Deploy the final version of the contract, maintaining compatibility with the previous versions.

Note: When deploying the updated versions of the contract, make sure to use the Transparent Proxy Pattern. This pattern involves deploying a proxy contract that delegates calls to the implementation contract. The proxy contract's address is used as the entry point for interacting with the contract, and it remains the same throughout the different versions. This allows for upgradability while maintaining a consistent address.

To perform testing, you can interact with the contract using the proxy address on the Goerli Etherscan. Ensure that all the features from Phases 1, 2, and 3 can be executed directly using the proxy address.

Please refer to the document provided in the resource section of the 8th February live class for detailed instructions on implementing the Transparent Proxy Pattern and using the Gnosis Multisignature wallet for upgradable smart contracts.
