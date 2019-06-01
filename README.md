# vue-js-starter-kit

This is an example client side wallet built in Vue.js which allows you to make interactions with the OMG network from the browser.

Before you get started, make sure you have a local instance of elixir-omg running or have access to an already deployed network. Feel free to build on top of the functionalities which you see here.

NOTE: 
- This kit is meant for development and demonstration purposes. It is not safe for production use.
- This example application is compatible with `elixir-omg v0.2`

## Initial Setup

Make sure you have access to the endpoints including Watcher, Childchain, address of the Plasma Contract and Web3 RPC endpoint. The wallet also requires an in-browser web3 wallet like MetaMask to sign transactions.

the endpoints for production deployment can be found [here](https://github.com/omisego/dev-portal/blob/master/guides/network_endpoints.md)

1. Installing dependencies by running `npm install` on the root directory

2. Open up the file config.js in your favorite text editor.

Replace the current configuration in config.js with your endpoints for `web3ProviderUrl`, `watcherUrl`, `childchainUrl`, `plasmaContractAddress`.

Save the config.js file.

3. Start the app by running `npm run dev`

## Running the Starter-kit

Open up your browser and navigate to `http://localhost:8080`, Make sure your Metamask is currently unlocked. You should be able to see your account balance on both Root chain and Child chain.

From here, you can perform 3 actions:

1. Deposit into the OMG Network: After 12 blocks confirmations, your Rootchain balance will be updated, click on the Refresh button. 

2. Transfer the funds on the OMG Network: Fill in the values for the Transfer fields and click Ok. Depending on the network congestion, you may have to wait for a little while for the transaction to be included in a block. Click on the Refresh balances button until your balance has been properly reflected.

3. Exit the funds back to Rootchain: Fill in an address that has funds in the OMG Network and click on OK, your exit period will start. Do note that the exit period will be varied based on the configuration of each `elixir-omg` deployment. After the certain amount of time has passed, you will be able to process the exit and receive your funds back.

NOTE: the current wallet does not offer a way to call `processExit()` yet.