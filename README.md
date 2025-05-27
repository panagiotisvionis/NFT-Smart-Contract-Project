# NFT Smart Contract Project

A project for developing, testing, and deploying Ethereum-based NFT smart contracts using **Hardhat** and **Solidity**.

## 🧱 Project Structure

```
nft-project/
├── contracts/           # Solidity contracts (e.g., MyNFT.sol)
├── scripts/             # Deployment and interaction scripts
├── test/                # Mocha/Chai tests for contracts
├── artifacts/           # Compiled contract outputs (auto-generated)
├── cache/               # Compiler cache (auto-generated)
├── node_modules/        # Installed npm dependencies
├── .env                 # Environment variables (e.g., private key, Infura)
├── .gitignore
├── hardhat.config.js    # Hardhat configuration
├── package.json         # Project metadata and dependencies
├── package-lock.json
└── README.md            # Project overview (you’re reading it!)
```

## 🚀 Quick Start

### 1. Install Dependencies

```bash
npm install
```

### 2. Compile Contracts

```bash
npx hardhat compile
```

### 3. Run Tests

```bash
npx hardhat test
```

### 4. Deploy to a Network

```bash
npx hardhat run scripts/deploy.js --network <network_name>
```

> Make sure you’ve set up `.env` with your private key and RPC URL before deploying.

## 📝 Example `.env` File

```
PRIVATE_KEY=your_private_key_here
INFURA_API_KEY=your_infura_project_id
```

## 🧪 Testing

Test files are located in the `test/` directory and use **Mocha** and **Chai**.

Example:

```javascript
describe("MyNFT", function () {
  it("Should deploy successfully", async function () {
    const MyNFT = await ethers.getContractFactory("MyNFT");
    const nft = await MyNFT.deploy();
    await nft.deployed();
    expect(nft.address).to.properAddress;
  });
});
```

## 🛠 Technologies Used

- [Hardhat](https://hardhat.org/)
- [Solidity](https://soliditylang.org/)
- [Ethers.js](https://docs.ethers.org/)
- [Infura](https://infura.io/) or [Alchemy](https://www.alchemy.com/)
- [Mocha](https://mochajs.org/)
- [Chai](https://www.chaijs.com/)

## 📄 License

This project is licensed under the **MIT License**.

## 👤 Author

Developed by **Panagiotis Vionis**  
Feel free to fork, contribute, or use it as a boilerplate for your NFT projects.