# Joining-the-Testnet-ALICE

# Recommended Requirements
- **A Linux server with 4 GB of RAM, dual-core CPU, 20GB of storage space**

# How to Join Alice

**1) Running the Node**
-  **Before installing a Muon node, one needs to [install Docker](https://docs.docker.com/engine/install/#server). To do so, you can use Install Docker Engine, where you should first choose your server's operating system, and then follow the installation instructions.**
- **The first step is to get the Muon docker-compose.yml :** 
```pyton
curl -o docker-compose.yml https://raw.githubusercontent.com/muon-protocol/muon-node-js/testnet/docker-compose-pull.yml
```

- ** Now the node can be run using the following command.**
```pyton
docker compose up -d
```
- **If this is run successfully, the node's status can be viewed by opening the following address in your browser:**
```pyton
http://<server-ip>:8000/status
```
The result should look like this:
![image](https://user-images.githubusercontent.com/61777095/223038665-3de9874b-b93e-4c13-b1d3-7cc771386122.png)
The highlighted address and peerId will be needed in the last stage of adding the node to the network (explained below).

**2) Adding the Node to the Network** 
- **To join ALICE, one needs to stake ALICE token. This dashboard is used for staking ALICE test token, and adding the node to the Testnet. Here is a step-by-step description:**
![image](https://user-images.githubusercontent.com/61777095/223038905-03277bdd-db4c-42cf-9fd8-d863c1d2f766.png)
- **As ALICE's node manager is deployed on BSC Testnet, this network should be added to your wallet before you can start adding the node. The "SWITCH NETWORK" button can be used to add and switch to this network.**  
![image](https://user-images.githubusercontent.com/61777095/223038965-86cdda61-bf9a-43f2-9951-e51b0245a31b.png)
- **Just as the network is switched to BSC, the following message appears if one does not have the gas tokens. Use the linked faucet to claim the required amount.**
![image](https://user-images.githubusercontent.com/61777095/223039012-664fd968-470a-4e62-9cb5-fc4eb98a0319.png)
- **After one has claimed the gas tokens, the first step is to mint the minimum required amount of ALICE token to run a node, which is 1000 tokens.**
![image](https://user-images.githubusercontent.com/61777095/223039070-99d8e85b-39fb-49cc-bbab-895dea83f2c0.png)
- **The node owner should then approve the staking contract to use the tokens.**
![image](https://user-images.githubusercontent.com/61777095/223039115-e3e4bc32-e203-429f-9c57-282ac1b86bbd.png)
- **Finally, the tokens are staked and the node is added to the network.** 
![image](https://user-images.githubusercontent.com/61777095/223039157-fbeeb929-be73-43c9-9112-86b78661166f.png)
- **The values for the fields Node Address and Peer Id are obtained from the node's status (explained above in "Running the Node"). (Click on the graphic to get a higher resolution.)**
![image](https://user-images.githubusercontent.com/61777095/223039214-9a9f7b91-0a63-4329-b22f-bff3fa41360a.png)
- **After the node is added and its transaction is confirmed, you are forwarded to a page that shows your node's information including the status.**
![image](https://user-images.githubusercontent.com/61777095/223039259-5a36c226-fa76-4f96-9ea8-514baa456377.png)
- **If the node is successfully added to the network, the status should be shown as "Active".**

