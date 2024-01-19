
# Avail contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Ethereum mainnet
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
WAVAIL
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Do you plan to support ERC1155?
No
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

No
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

No
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
Admins are TRUSTED.
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
Proxy admin and DEFAULT_ADMIN_ROLE is TRUSTED, since they can upgrade contracts at will.

___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
PAUSER_ROLE is responsible for pausing all contract functionality. They should not be able to carry out any other action.
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
NA
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
NA
___

### Q: Please provide links to previous audits (if any).
NA
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
* Avail bridge pallet
* Succinct Vectorx proof generation
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
Mostly yes, out of scope includes:
* Liveness bugs
* Pausing
* Executing an emergency withdrawal
Things that are in scope include:
* Forgery of proofs, for data attestation or messaging
___

### Q: Do you expect to use any of the following tokens with non-standard behaviour with the smart contracts?
No
___

### Q: Add links to relevant protocol resources
* https://avail-project.notion.site/The-Avail-Bridge-Public-Copy-a00c2aa4937d496ea346d02a6bb119ff
* https://docs.availproject.org
* https://github.com/availproject/avail/pull/362
* https://github.com/succinctlabs/vectorx/tree/main
* https://alpha.succinct.xyz/avail/vectorx
___



# Additional Context

We are particularly looking for novel attacks that are able to show forgery of proofs, either for data attestation or the arbitrary message bridge. We are also looking for any attack vectors which cause loss of user funds and/or unexitable assets. These should not be any attacks which are due to admin misconfiguration, as those are existing trusted attack vectors.

We also have ongoing testnet challenges where you can attack the treasury (this is not part of the audit and is instead covered by a separate reward structure): https://docs.availproject.org/clash-of-nodes/challenges

# Audit scope


[contracts @ ce7d2408158d8d74fc3bbf6c1dbe48e675e36579](https://github.com/availproject/contracts/tree/ce7d2408158d8d74fc3bbf6c1dbe48e675e36579)
- [contracts/src/AvailBridge.sol](contracts/src/AvailBridge.sol)
- [contracts/src/MessageReceiver.sol](contracts/src/MessageReceiver.sol)
- [contracts/src/WrappedAvail.sol](contracts/src/WrappedAvail.sol)
- [contracts/src/lib/Merkle.sol](contracts/src/lib/Merkle.sol)

