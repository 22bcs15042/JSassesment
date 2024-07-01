// Step 1: Create a variable that can hold a number of NFTs
let nftCollection = [];

// Step 2: Create a mintNFT function to generate and store NFT metadata
function mintNFT(name, creator, description, imageUrl) {
    const nft = {
        name: name,
        creator: creator,
        description: description,
        imageUrl: imageUrl
    };
    nftCollection.push(nft);
}

// Step 3: Create a listNFTs function to print all NFTs metadata
function listNFTs() {
    nftCollection.forEach((nft, index) => {
        console.log(`NFT #${index + 1}`);
        console.log("Name: " + nft.name);
        console.log("Creator: " + nft.creator);
        console.log("Description: " + nft.description);
        console.log("Image URL: " + nft.imageUrl);
        
    });
}

// Step 4: Create a getTotalSupply function to return the number of NFTs created
function getTotalSupply() {
    return nftCollection.length;
}

// Example usage:
mintNFT("Digital Art Piece", "alfonso", "A beautiful piece of digital art.", "http://example.com/image1.png");
mintNFT("Virtual Real Estate", "sherlin", "A prime piece of virtual real estate.", "http://example.com/image2.png");

console.log("Listing all NFTs:");
listNFTs();

console.log("Total NFTs minted: " + getTotalSupply());
