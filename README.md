# SolCV

## Rationale 
SolCV is a fast and easy way to create and distribute your own business cards on Solana. With recent cNFT and state compression advancements, the cost of minting NFT's has become extremely affordable, making business cards a powerful use case for compressed NFTs. 

## Setup
- Get started by cloning the repo in your terminal by running `https://github.com/meta-lite/cNFT-Business-Cards.git`
- Before we can spin up the minting page, you will need to create a new project with [Underdog Protocol](https://www.underdogprotocol.com/products/minting-api). Use [Canva](https://www.canva.com/) to spin up your business card and download as PNG
- Open `index.html` in your favorite development environment. I recommend [VS Code](https://code.visualstudio.com/). Once VSCode is up and running install [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- On line 26, add a photo of your business card: `<img src="HERE"`
- On line 54, add your [Underdog Protocol](https://www.underdogprotocol.com/) API Key
- On lines 57 to 63, add your NFT info to replace each instance of `<>`:
```
        body: JSON.stringify({
            receiverAddress: inputVal,
            name: '<>',
            symbol: '<>',
            description: '<>',
            image: '<>',
            externalUrl: '<>'
        })
```
- Finally, on line 66, add your Underdog Project Link: `fetch('<Underdog Project Link>', options)`

## DEMO 
My personal version is live and hosted [here](https://meta-light.vercel.app/card.html). Mint a card, no wallet connection required. 

## Future
I want to build SolCV into a full service CV generation platform. Here's my next set of features to tackle: 

- Store social contact data (Backpack username, Dialect Username, Twitter, Discord, .sol etc) as metadata
- xNFT app that acts as an Address Book for collected SolCVs
- Potentially make some of these soulbound? Does this count as spam?
- Generate image straight from frontend


