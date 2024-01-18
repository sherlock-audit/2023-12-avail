
# Avail contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

# Additional Context

We are particularly looking for novel attacks that are able to show forgery of proofs, either for data attestation or the arbitrary message bridge. We are also looking for any attack vectors which cause loss of user funds and/or unexitable assets. These should not be any attacks which are due to admin misconfiguration, as those are existing trusted attack vectors.

We also have ongoing testnet challenges where you can attack the treasury (this is not part of the audit and is instead covered by a separate reward structure): https://docs.availproject.org/clash-of-nodes/challenges

# Audit scope


[contracts @ ce7d2408158d8d74fc3bbf6c1dbe48e675e36579](https://github.com/availproject/contracts/tree/ce7d2408158d8d74fc3bbf6c1dbe48e675e36579)
- [contracts/src/AvailBridge.sol](contracts/src/AvailBridge.sol)
- [contracts/src/MessageReceiver.sol](contracts/src/MessageReceiver.sol)
- [contracts/src/WrappedAvail.sol](contracts/src/WrappedAvail.sol)
- [contracts/src/lib/Merkle.sol](contracts/src/lib/Merkle.sol)

