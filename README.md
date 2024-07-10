# NFT Collection

This project demonstrates a simple implementation of an NFT (Non-Fungible Token) collection using JavaScript. The script includes functions to mint new NFTs, list all NFTs, and get the total supply of NFTs created.

## Features

- **Mint NFTs**: Generate and store NFT metadata.
- **List NFTs**: Print all NFTs metadata.
- **Get Total Supply**: Return the number of NFTs created.

## Code Overview

### Step 1: Create a variable to hold a number of NFTs
```javascript
let nftCollection = [];
###Step 2: Create a mintNFT function to generate and store NFT metadata
javascript
Copy code
function mintNFT(name, creator, description, imageUrl) {
    const nft = {
        name: name,
        creator: creator,
        description: description,
        imageUrl: imageUrl
    };
    nftCollection.push(nft);
}
Step 3: Create a listNFTs function to print all NFTs metadata
javascript
Copy code
function listNFTs() {
    nftCollection.forEach((nft, index) => {
        console.log(`NFT #${index + 1}`);
        console.log("Name: " + nft.name);
        console.log("Creator: " + nft.creator);
        console.log("Description: " + nft.description);
        console.log("Image URL: " + nft.imageUrl);
    });
}
Step 4: Create a getTotalSupply function to return the number of NFTs created
javascript
Copy code
function getTotalSupply() {
    return nftCollection.length;
}
Example Usage
javascript
Copy code
mintNFT("Digital Art Piece", "alfonso", "A beautiful piece of digital art.", "http://example.com/image1.png");
mintNFT("Virtual Real Estate", "sherlin", "A prime piece of virtual real estate.", "http://example.com/image2.png");

console.log("Listing all NFTs:");
listNFTs();

console.log("Total NFTs minted: " + getTotalSupply());
