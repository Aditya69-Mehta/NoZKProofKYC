# NoZKProofKYC

A decentralized Know Your Customer (KYC) system built on Ethereum. This smart contract enables users to request KYC, and authorized verifiers to approve, reject, or revoke KYC status. It does not use Zero-Knowledge Proofs and demonstrates a basic on-chain identity verification flow.

## 🔍 Features

- On-chain KYC request and verification
- Role-based access (Owner, Verifier, User)
- Event logs for all actions
- Public KYC status visibility

## 🛠 Tech Stack

- Solidity
- Hardhat (recommended for testing and deployment)
- OpenZeppelin (for ownership and access control)

## 🧱 Contract Roles

- **Owner**: Can add or remove verifiers.
- **Verifier**: Can approve, reject, or revoke KYC requests.
- **User**: Any wallet address that can submit a KYC request.

## 🔄 KYC Workflow

1. `Unverified` – Default status for all users
2. `Pending` – After a user requests KYC
3. `Verified` – After a verifier approves the request
4. `Rejected` – After a verifier rejects the request
5. `Unverified` – If a verified user’s KYC is revoked

## 🔧 Functions

### Users

- `requestKYC(string name, uint8 age, string userId)`
  - Request KYC verification

### Verifiers (Only Verifier)

- `approveKYC(address user)`
- `rejectKYC(address user, string reason)`
- `revokeKYC(address user)`

### Owner

- `addVerifier(address verifier)`
- `removeVerifier(address verifier)`

### View Functions

- `getUserInfo(address user) → (string name, uint8 age, KYCStatus)`
- `isUserVerified(address user) → bool`
- `isVerifier(address verifier) → bool`

## 📄 License

MIT
