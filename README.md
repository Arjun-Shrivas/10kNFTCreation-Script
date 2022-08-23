

Base code is from [hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine)

Minting uses [NFTPort](https://nftport.xyz)

### npm not recognized

You have not installed [node.js](https://nodejs.org) properly. Be sure to follow the installation instructions from their download page for your specific operating system. And restart your computer after installation.

### Images not lining up

Be sure that every layer is the same size. If you want the resulting image to be 512x512, then each layer needs to be 512x512. This will ensure that everything lines up properly.

### Only the last image shows up

This is because you are not using `.png` images. `.jpg` or any other type will not work. `.png` has transparency which means there is no background and things behind it will show through. 

### ES Module Error \[ERR_REQUIRE_ESM\]

`node-fetch` was at version 2. It was recently updated to version 3 and no longer supports the `require` syntax. 

Fortunately, it's an easy fix. Just type these commands into the terminal:

- `npm uninstall node-fetch`
- `npm install node-fetch@2`

### Any sort of "path" error

Ensure that your layer names in the `config.js` file match exactly to your layer folder names. Also, remove any `-` (hyphens) from your file names.

### "Quota Limit Reached" or "Too many requests" errors

There have been some changes made to the code from the original video resulting from some errors when uploading files, metadata, and minting using NFTPort. Depending on your plan, Free vs Community, there are rate limits. 

To fix these issues, I've updated the code to include a timeout that will allow the files to be uploaded at a slower rate, instead of all at once, eliminating these errors.  

# 🚀 Quick Start

📄 Clone or fork `ethereum-boilerplate`:

```sh
git clone https://github.com/Arjun-Shrivas/10kNFTCreation-Script.git
```

💿 Install all dependencies:

```sh
cd ethereum-boilerplate
npm install
```

✏ Rename `.env.example` to `.env` in the main folder and provide your `appId` and `serverUrl` from Moralis ([How to start Moralis Server](https://docs.moralis.io/moralis-server/getting-started/create-a-moralis-server))
Example:

```jsx
AUTH=xxx-xxxx-xxxx-xxxx # Past here your NFTPort API KEY
CONTRACT_ADDRESS=xx-xxx-xxx-xxx-xx # Past here Your Deployed Contract Address that placed in NFTPORT  
MINT_TO_ADDRESS=xx-xxx-xxx-xxx-xxx # Past Here Your Wallet Address
CHAIN='rinkeby'          # Type your desire Chain Name 
```

🚴‍♂️ you can Complete your NFT upload Process  Only in  Three Steps:

step 1: -
```node utils/nftport/uploadFiles.js
```


step 2: -
```node utils/nftport/uploadMetas.js
```


step 3: -
```node utils/nftport/mint.js
```

## Reference the [video](https://youtu.be/AaCgydeMu64) for more details. All commands to upload and mint are the same. 
