## 8. Modify the Ported dApp so it Supports Ethereum Assets via Force Bridge

## Task Submission

### 1.a. Screenshots of Layer 2 DApp with Force Bridge support. <br><br>
![image](https://user-images.githubusercontent.com/5003779/129457756-66aa0183-ecd8-4f3c-b128-dd5f091eb5ba.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129457449-f8afa64a-f8a3-4f19-9fab-d0ce4867c3bf.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129457502-dd0941eb-ddc6-45c5-bdb4-81ab6552d16d.png) <br><br><br><br>
![image](https://user-images.githubusercontent.com/5003779/129457526-362b8809-16c3-42cb-99ec-ca7bb49714b0.png) <br><br>
### 1.b. Video<br><br>
[![image](https://img.youtube.com/vi/n1qOWvMRi_I/0.jpg)](https://youtu.be/n1qOWvMRi_I)
### 2. Links <br>
   🟦 My implementation: https://github.com/stevenhva/tasks-dapp-polyjuice-force-bridge <br>
   🟦 Origin repository #1: https://github.com/AndrewJBateman/blockchain-ethereum-contract.git <br>
   🟦 Origin repository #2: https://github.com/x777/todo-dapp-polyjuice <br><br>
### 3.a. Hash of the deployment transaction <br>
   🟣 0xfbb9e98f94325179d47459334dfa2814a316269a52f42928f6a630b3af9a1cfc <br><br>
### 3.b. Deployed contract address <br>
   ⚪ 0x17148DC771e7192701afB2c54F70E47651b479E3 <br><br>
### 3.c. ABI of deployed smart contract <br>
   🟢 [ { "inputs": [], "stateMutability": "nonpayable", "type": "constructor" }, { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "uint256", "name": "id", "type": "uint256" }, { "indexed": false, "internalType": "string", "name": "title", "type": "string" }, { "indexed": false, "internalType": "string", "name": "description", "type": "string" }, { "indexed": false, "internalType": "bool", "name": "done", "type": "bool" }, { "indexed": false, "internalType": "uint256", "name": "createdAt", "type": "uint256" } ], "name": "TaskCreated", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "uint256", "name": "id", "type": "uint256" }, { "indexed": false, "internalType": "bool", "name": "done", "type": "bool" } ], "name": "TaskToggledDone", "type": "event" }, { "inputs": [], "name": "taskCounter", "outputs": [ { "internalType": "uint256", "name": "", "type": "uint256" } ], "stateMutability": "view", "type": "function" }, { "inputs": [ { "internalType": "uint256", "name": "", "type": "uint256" } ], "name": "tasks", "outputs": [ { "internalType": "uint256", "name": "id", "type": "uint256" }, { "internalType": "string", "name": "title", "type": "string" }, { "internalType": "string", "name": "description", "type": "string" }, { "internalType": "bool", "name": "done", "type": "bool" }, { "internalType": "uint256", "name": "createdAt", "type": "uint256" } ], "stateMutability": "view", "type": "function" }, { "inputs": [ { "internalType": "string", "name": "_title", "type": "string" }, { "internalType": "string", "name": "_description", "type": "string" } ], "name": "createTask", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "uint256", "name": "_id", "type": "uint256" } ], "name": "toggleDone", "outputs": [], "stateMutability": "nonpayable", "type": "function" } ]
