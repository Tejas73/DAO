# DAO Smart Contract

This smart contract, named DAO (Decentralized Autonomous Organization), is built on the Ethereum blockchain. It enables the creation and management of proposals within the organization, allowing investors to contribute funds, vote on proposals, and execute approved proposals.

## Features

- Investors can contribute funds to the DAO and receive shares in proportion to their contribution.
- Investors can redeem their shares and receive the corresponding amount of funds.
- Investors can transfer their shares to other investors.
- The manager of the DAO can create proposals for funding specific initiatives.
- Investors can vote on proposals within a specified voting time.
- Approved proposals can be executed by the manager, transferring the allocated funds to the designated recipient.
- The DAO enforces a quorum requirement to ensure majority support for proposal execution.

## Smart Contract Structure

The smart contract consists of the following key components:

- `Proposal`: A struct defining the properties of a proposal, including an ID, description, funding amount, recipient address, vote count, end timestamp, and execution status.
- `isInvestor`: A mapping that keeps track of whether an address is an investor in the DAO.
- `numOfshares`: A mapping that stores the number of shares held by each investor.
- `isVoted`: A mapping that records whether an investor has voted on a particular proposal.
- `investorsList`: An array that maintains a list of all investors in the DAO.
- `totalShares`: A variable that tracks the total number of shares issued.
- `availableFunds`: A variable that represents the available funds in the DAO.
- `contributionTimeEnd`, `nextProposalId`, `voteTime`, `quorum`, and `manager`: Variables that control various aspects of the DAO, such as the contribution period, proposal ID counter, voting duration, quorum requirement, and manager address.

## Getting Started

To interact with the DAO smart contract, you can deploy it on the Ethereum network using a development tool like Truffle or Remix IDE. After deployment, you can utilize the following functions:

- `contribution()`: Investors can contribute funds to the DAO.
- `reedemShare(uint amount)`: Investors can redeem their shares and receive the corresponding amount of funds.
- `transferShare(uint amount, address to)`: Investors can transfer their shares to another investor.
- `createProposal(string calldata description, uint amount, address payable receipient)`: The manager can create proposals for funding.
- `voteProposal(uint proposalId)`: Investors can vote on proposals.
- `executeProposal(uint proposalId)`: The manager can execute approved proposals.
- `ProposalList()`: Retrieves a list of all proposals in the DAO.
- `InvestorList()`: Retrieves a list of all investors in the DAO.

## Note

Please ensure that appropriate security measures are taken when deploying and interacting with the DAO smart contract. It's crucial to thoroughly review and test the contract to identify and mitigate potential vulnerabilities.

Feel free to explore and enhance this DAO smart contract for your specific decentralized organization needs.

# License

This smart contract is licensed under the GNU General Public License v3.0.
