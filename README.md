mintNFT(name, description, image) {
    this.mintedNFTs.push({ name, description, image });
}

listNFTs() {
    if (!this.mintedNFTs.length) {
        console.log("No NFTs minted yet!");
        return;
    }

    this.mintedNFTs.forEach(nft => {
        console.log("Name:", nft.name);
        console.log("Description:", nft.description);
        console.log("Image:", nft.image);
    });
}

getTotalSupply() {
    return this.mintedNFTs.length;
}
