# My Custom NFT

A simple javascript program to demonstrate the use of creating a local nft variable to store nft data in it by calling the mintNFT function by passing the required parameters for it, listNFT function which will loop through the nft variable and print the metadata and finally the getTotalSupply function to list the nft length till now stored in the nft variable. 

## Description

The program features the following things -
1. variables to store the nft details
2. a mintNFt function which will accept the metadata and store it in the array
3. getTotalSupply function to print the amount of nft we have minted till now

## Getting Started

### Executing program

To run this program, you can use online javascript compiler or vs code if you have node installed locally. Just copy paste the content of the Custom.js file and run it in the online IDE. 

```javascript
/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created

*/

// create a variable to hold your NFT's
const NFT = []
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT (brand, category, enginecapacity, topspeed) {
    const nft = {
        "brand":brand, 
        "category":category,
        "enginecapacity":enginecapacity,
        "topspeed":topspeed
    }
    NFT.push(nft);
    console.log("Minted " + brand);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {
    for(let i=0; i<NFT.length;i++){
        console.log(NFT[i]);
    }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log(NFT.length);
}

// call your functions below this line
mintNFT("Himalayan","adventure bike","411cc","345kmph");
listNFTs();
getTotalSupply();
```
## Authors

Smriti Raman

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
