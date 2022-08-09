# solana-nft-collection
Mint NFTs with Solana and Metaplex

# To get started:
1. cd into the app folder
2. Run npm install at the root of your directory
3. Run npm run start to start the project

# Pre-requisites:
1. Phantom Wallet
2. Install Metaplex candy machine (at the root ~) (git clone -b v1.1.1 https://github.com/metaplex-foundation/metaplex.git) && yarn install --cwd ~/metaplex/js/htt
3. Solana-Cli
4. Metaplex-Cli
5. git version > 2.3.1
6. node version > 14.17.0
7. yarn version > 1.22.11
8. ts-node version > 10.2.1

# To deploy on blockchain:
1. solana-keygen new --outfile ~/.config/solana/devnet.json
2. solana-config set --keypair ~/.config/solana/devnet.json
3. solana config set --url devnet
4. solana airdrop 2 ( if you dont have any sol)
5. ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts upload -e devnet -k ~/.config/solana/devnet.json -cp config.json ./assets (be sure to be in the root folder of the app)
6. ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts verify_upload -e devnet -k ~/.config/solana/devnet.json
7. ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts update_candy_machine -e devnet -k ~/.config/solana/devnet.json