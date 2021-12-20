# Onboard Wallet Module - [WalletLink](https://walletlink.org/)

## Options

```typescript
type WalletLinkOptions = {
  darkMode: boolean // default = false
}
```

## Usage

```typescript
import Onboard from '@bn-onboard/core'
import walletLinkModule from '@bn-onboard/walletlink'

// initialize the module with options
const walletLink = walletLinkModule({ darkMode: true })

// can also initialize with no options...
// const walletLink = walletLinkModule()

const onboard = Onboard({
  // ... other Onboard options
  wallets: [
    walletLink
    //... other wallets
  ]
})

const connectedWallets = await onboard.connectWallet()
console.log(connectedWallets)
```