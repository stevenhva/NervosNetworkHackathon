# 7. Port an Existing Ethereum dApp to Polyjuice

## Task Submission

### 1.a. Screenshots <br><br>
![image](https://user-images.githubusercontent.com/5003779/129417492-02e0cf1c-0d05-45b1-903b-d32b852b4bd1.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129417468-4f20f4d6-fc28-4a1f-b661-592ce0ae8766.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129417430-3fa251e5-1fc2-4f1c-b320-d36e5e5e3732.png) <br><br>
### 1.b. Video<br><br>
[![image](https://img.youtube.com/vi/Vb_uVLi2XiA/0.jpg)](https://youtu.be/Vb_uVLi2XiA)
### 2. Links <br>
   🟦 My implementation: https://github.com/stevenhva/tasks-dapp-polyjuice <br>
   🟦 Origin repository #1: https://github.com/AndrewJBateman/blockchain-ethereum-contract.git <br>
   🟦 Origin repository #2: https://github.com/lqne/polyjuice-dapp-port.git <br><br>
### 3.a. Hash of the deployment transaction <br>
   🟣 0x15fc344789bb80689f0fb6b58a4608b62fb461207ea7804c8fa2dadc8305220b <br><br>
### 3.b. Deployed contract address <br>
   ⚪ 0xBA40af9218713138314De80340B842C1fFf3Ba16 <br><br>
### 3.c. ABI of deployed smart contract <br>
   🟢 [
    {
      "inputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "id",
          "type": "uint256"
        },
        {
          "indexed": false,
          "internalType": "string",
          "name": "title",
          "type": "string"
        },
        {
          "indexed": false,
          "internalType": "string",
          "name": "description",
          "type": "string"
        },
        {
          "indexed": false,
          "internalType": "bool",
          "name": "done",
          "type": "bool"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "createdAt",
          "type": "uint256"
        }
      ],
      "name": "TaskCreated",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "id",
          "type": "uint256"
        },
        {
          "indexed": false,
          "internalType": "bool",
          "name": "done",
          "type": "bool"
        }
      ],
      "name": "TaskToggledDone",
      "type": "event"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "taskCounter",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "tasks",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "id",
          "type": "uint256"
        },
        {
          "internalType": "string",
          "name": "title",
          "type": "string"
        },
        {
          "internalType": "string",
          "name": "description",
          "type": "string"
        },
        {
          "internalType": "bool",
          "name": "done",
          "type": "bool"
        },
        {
          "internalType": "uint256",
          "name": "createdAt",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "internalType": "string",
          "name": "_title",
          "type": "string"
        },
        {
          "internalType": "string",
          "name": "_description",
          "type": "string"
        }
      ],
      "name": "createTask",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_id",
          "type": "uint256"
        }
      ],
      "name": "toggleDone",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ]
