# Imali Admin Panel 🚀

A production-ready **Web3 Admin Dashboard** for DeFi platforms and token projects — built with **React**, **Ethers.js**, **GA4**, and **Looker Studio**.

[![NPM version](https://img.shields.io/npm/v/imali-admin-panel.svg)](https://www.npmjs.com/package/imali-admin-panel)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/IMALI-DEFI/imali-admin-panel.svg?style=social)](https://github.com/IMALI-DEFI/imali-admin-panel)

---

## ✨ Features

- ✅ Wallet connect (MetaMask + WalletConnect ready)
- ✅ Smart contract actions: Mint, Airdrop, Buyback, Add Liquidity
- ✅ GA4 pageview + event tracking
- ✅ Looker Studio embedded dashboard
- ✅ Social sharing across major platforms
- ✅ Schedule posts and log internal actions

---

## 🔧 Installation

```bash
npm install imali-admin-panel
```

---

## 🚀 Usage Example

```jsx
import { AdminPanel, WalletProvider } from "imali-admin-panel";

function App() {
  return (
    <WalletProvider>
      <AdminPanel />
    </WalletProvider>
  );
}
```

---

## 📊 Live Analytics

This panel includes an embedded Looker Studio dashboard with live traffic and performance metrics.  
> You can replace the `iframe` URL with your own GA4-connected dashboard.

---

## 🔌 Contract Integration

Update `getContractInstance.js` with your deployed contract ABIs and addresses.  
Example:
```js
export const getContractInstance = async (name, signerOrProvider) => {
  const address = {
    IMALIToken: "0x...",
    Lending: "0x...",
    AirdropDistributor: "0x...",
    LiquidityManager: "0x...",
    Buyback: "0x..."
  }[name];

  const abi = await import(`../abis/${name}.json`);
  return new ethers.Contract(address, abi.default, signerOrProvider);
};
```

---

## 📸 Screenshots

![AdminPanel](https://user-images.githubusercontent.com/123456789/imaginary-dashboard.png)

---

## 💸 License

MIT — Free to modify and resell with attribution.

---

## 🔗 Links

- 🌐 [Live Demo](https://imali-defi.com)
- 🛠 [Smart Contract Repo](https://github.com/IMALI-DEFI/contracts)
- 📦 [NPM Package](https://www.npmjs.com/package/imali-admin-panel)

---
Made with 🧠 by [Wayne Griffin](https://linkedin.com/in/wayne-l-griffin-mba)
