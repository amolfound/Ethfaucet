Designed a node js based ethereum faucet. Requests signed by client (using ethereum priv key) can be made by the client and sent to faucetServer which verifies the request and uses a web3 wallet to transfer funds to client.

Resources:

Wallet.js:
    wrapper around web3 for basic calls and account initialisation
    functions like getBalance, transferEth, signTxn, waitForTxn (n confirmations)

FaucetServer.js:
    http server which validates eth request(signed using eth priv keys) from clients. Has a replay attack prevention scheme with message salts and timestamps

FaucetClient.js:
    prepares a signed request to make ether requests to faucetServer
