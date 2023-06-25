Steps to Create ERC-20 Tokens:-

Create a Metamask Account:-
1) Create a Account on Metamask Wallet using the Metamask extension.
2) In Metamask go to settings and connect the wallet to Goerli Test-Network.
3) Currently we do not have any GoerliETH so we need to mine it because it will be needed as gas fees while deploying our token.
4) From the website https://goerli-faucet.pk910.de/ we can mine GoerliETH by providing our metamask wallet address. we need to mine more than 0.01.

Using 20lab:-
1) https://20lab.app/ - Visit the website(20lab an ERC-20 token generator tool)
2) Click on Open App, and click on start.
3) We need to click on Connect Wallet and select our wallet which needs to be connected to 20lab for creating a token and its deployment.
4) Choose Goerli(Testnet) and we can check out the tutorial given for generating our first ERC-20 token on 20lab.app.
5) Provide the basic information such as token name, token symbol, initial suppy, decimals etc.
6) Choose other required features for your token and save it.
7) Then we need to validte and compile it.
8) Now we can see our token name and address in the dashboard

Now check your token on https://goerli.etherscan.io/ foe seeing our transaction history of our token

# ledger-fabric
To initiate the first Hyperledger Fabric network, we will utilize the Fabric-samples repository. This repository consists of CLI tool binaries and Fabric Docker Images, which are essential for comprehending and utilizing the fundamentals of Fabric. Before commencing the project, it is necessary to install the following dependencies:

# 1.Install Docker

    sudo apt-get -y install docker-compose

# 2. Install Golang-go

    sudo apt install golang-go

# 3. Install jq

    sudo apt install jq

# 4. Install Node/java

    sudo apt install npm
    npm install node

# 5. Installing Fabric-samples Repository

    curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh
    
Then you can pull docker containers by running one of these commands:

    ./install-fabric.sh docker samples
    ./install-fabric.sh d s 

To install binaries for Fabric samples you can use the command below:

    ./install-fabric.sh binary
    
# Building First Network

1.Navigate through the Fabric-samples folder and then through the Test network folder where you can find script files using these we can run our network.

    cd fabric-samples/test-network

2.We would be running ./network.sh down command to remove any previous network containers or artifacts that still exist. 

    ./network.sh down

3.  we can bring up a network using the following command. This command creates a fabric network that consists of two peer nodes and one ordering node.

    ./network.sh up
