## FX Swap Token List
FX Swap Token List is a specification for list of token metadata (e.g. address and decimals) that can be used by dApp interface. 

This repository is a comprehensive collection of tokens on FX Swap.

Token logos are stored according to their f(x) EVM address under the `Tokens/` directory and the images are stored in the format `<Token-Address>/logo.png`.

### General Requirements
1. Token should be verified on FX Explorer [Mainnet](https://explorer.functionx.io/) or [Testnet](https://testnet.explorer.functionx.io/)
2. Token must be on the f(x) EVM

### Adding Token to the Existing List
1. Add an entry in the `tokens` field.
- Example: 
```
{
    "name": "Pundi X Token",
    "chainId": 530,
    "symbol": "PUNDIX",
    "decimals": 18,
    "address": "0xd567B3d7B8FE3C79a1AD8dA978812cfC4Fa05e75",
    "logoURI": "https://raw.githubusercontent.com/YP010/FXSwap-TokenList/main/Tokens/0xd567B3d7B8FE3C79a1AD8dA978812cfC4Fa05e75/logo.png"
}
```

2. Update the `timestamp` field to the current timestamp.

3. Update the `version` field to adhere to semantic versioning. 
- Increment major version when tokens are removed or when changing a token address or chain ID
- Increment minor version when tokens are added
- Increment patch version when tokens on the list have minor details changed (E.g. name, symbol, logoURI, decimals)

### Adding Token Logo
1. Create a new directory in `Tokens\` directory, named using the [checksum token address](https://web3js.readthedocs.io/en/v1.7.1/web3-utils.html#tochecksumaddress).
2. Add token image as file named logo.png inside the directory.
3. Image should not be larger than 20 KB.
