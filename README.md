[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg?style=flat-square)](https://github.com/standard/semistandard)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

# hashicorp vault signing manager

Polymesh SDK compatible signing manager that interacts with a Hashicorp Vault transit engine for signing transactions.

## Usage

```typescript
import { HashicorpVaultSigningManager } from '@polymeshassociation/hashicorp-vault-signing-manager';
import { Polymesh } from '@polymeshassociation/polymesh-sdk';

// setup
const signingManager = new HashicorpVaultSigningManager({
  // URL of the Vault's transit engine
  url: 'https://my-hosted-vault.io/v1/transit',
  // authentication token
  token: 'willNeverTell',
});

const polymesh = await Polymesh.connect({
  nodeUrl,
  signingManager,
});
```
