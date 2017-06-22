# PayMob Blockchain

## Description

This is a project developed for PayMob that simulates how blockchain technology can be used between banks around the world

## Prerequisits

Make sure that you have installed the Multichain Blockchain on the system you will be running on. [Click here for Installations steps](http://www.multichain.com/download-install/)

This project uses Python3 and [Savoir](https://github.com/DXMarkets/Savoir), a wrapper for the Multichain blockchain in python.

You can install Savoir using pip `pip3 install Savoir`

## Configuration

The next step is to start your blockchain and connect the nodes to each other. This can easily be done by following steps 1 and 2 that can be found on the [Multichain Getting Started Guide](http://www.multichain.com/getting-started/)

Each node on the blockchain must contain 3 files:

1. Transactions.py 
2. background_check.py
3. Bank_Records.json

Now you have to configure the file for each node according to the current blockchain. These are lines 8-21 in the Transaction.py file and lines 5-13 in the background_check.py file. 

The JSON file have to follow the same format as shown in the example JSON in the repository.

Next a stream must be started by typing into the console `multichain-cli [chain-name] create stream [stream-name] true`

This stream must then be subscribed to by typing `multichain-cli [chain-name] subscribe [stream-name]`

Finally the last thing is to issue assets, this can be done by issuing assets to the main node by using `issue [address] [asset-name] [amount]`

This can all be found in more detail on the getting started guide parts 4 and 6.

## Usage 

Congradulations, if all goes well you have sucessfully implemented the blockchain.

All you have to do now is run `python3 background_check.py &` to run the script in the background

and now run `python3 Transactions.py` for the main menu where you can:

1. Add Account
2. Edit Account
3. Search Account
4. Payment Request
5. See total balance in PMC(PayMobCoins)
6. See internal balances in local currency

Best of luck, any questions, you can email me at fibrahim@stevens.edu
