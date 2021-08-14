# 8. Modify the Ported dApp so it Supports Ethereum Assets via Force Bridge

## Task Submission


The address of the SUDT-ERC20 Proxy Contract that you deployed (in text format).
A link to the GitHub repository with your EVM application that integrates Force Bridge support.

### 1.a. Screenshots of Layer 2 DApp with Force Bridge support. <br><br>
![image](https://user-images.githubusercontent.com/5003779/129457455-69a72427-e296-49bd-b7cb-0a6f178bbaaf.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129457449-f8afa64a-f8a3-4f19-9fab-d0ce4867c3bf.png) <br>
![image](https://user-images.githubusercontent.com/5003779/129457502-dd0941eb-ddc6-45c5-bdb4-81ab6552d16d.png) ![image](https://user-images.githubusercontent.com/5003779/129457526-362b8809-16c3-42cb-99ec-ca7bb49714b0.png) <br><br>
### 2. Links <br>
   🟦 My implementation: https://github.com/stevenhva/tasks-dapp-polyjuice-force-bridge <br>
   🟦 Origin repository #1: https://github.com/AndrewJBateman/blockchain-ethereum-contract.git <br>
   🟦 Origin repository #2: https://github.com/x777/todo-dapp-polyjuice <br><br>
### 3.a. Hash of the deployment transaction <br>
   🟣 0xfbb9e98f94325179d47459334dfa2814a316269a52f42928f6a630b3af9a1cfc <br><br>
### 3.b. Deployed contract address <br>
   ⚪ 0x17148DC771e7192701afB2c54F70E47651b479E3 <br><br>
### 3.c. ABI of deployed smart contract <br>
   🟢 {
  "contractName": "TasksContract",
  "abi": [
    {
      "inputs": [],
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
      "inputs": [],
      "name": "taskCounter",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
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
      "stateMutability": "view",
      "type": "function"
    },
    {
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
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "_id",
          "type": "uint256"
        }
      ],
      "name": "toggleDone",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ],
  "metadata": "{\"compiler\":{\"version\":\"0.8.0+commit.c7dfd78e\"},\"language\":\"Solidity\",\"output\":{\"abi\":[{\"inputs\":[],\"stateMutability\":\"nonpayable\",\"type\":\"constructor\"},{\"anonymous\":false,\"inputs\":[{\"indexed\":false,\"internalType\":\"uint256\",\"name\":\"id\",\"type\":\"uint256\"},{\"indexed\":false,\"internalType\":\"string\",\"name\":\"title\",\"type\":\"string\"},{\"indexed\":false,\"internalType\":\"string\",\"name\":\"description\",\"type\":\"string\"},{\"indexed\":false,\"internalType\":\"bool\",\"name\":\"done\",\"type\":\"bool\"},{\"indexed\":false,\"internalType\":\"uint256\",\"name\":\"createdAt\",\"type\":\"uint256\"}],\"name\":\"TaskCreated\",\"type\":\"event\"},{\"anonymous\":false,\"inputs\":[{\"indexed\":false,\"internalType\":\"uint256\",\"name\":\"id\",\"type\":\"uint256\"},{\"indexed\":false,\"internalType\":\"bool\",\"name\":\"done\",\"type\":\"bool\"}],\"name\":\"TaskToggledDone\",\"type\":\"event\"},{\"inputs\":[{\"internalType\":\"string\",\"name\":\"_title\",\"type\":\"string\"},{\"internalType\":\"string\",\"name\":\"_description\",\"type\":\"string\"}],\"name\":\"createTask\",\"outputs\":[],\"stateMutability\":\"nonpayable\",\"type\":\"function\"},{\"inputs\":[],\"name\":\"taskCounter\",\"outputs\":[{\"internalType\":\"uint256\",\"name\":\"\",\"type\":\"uint256\"}],\"stateMutability\":\"view\",\"type\":\"function\"},{\"inputs\":[{\"internalType\":\"uint256\",\"name\":\"\",\"type\":\"uint256\"}],\"name\":\"tasks\",\"outputs\":[{\"internalType\":\"uint256\",\"name\":\"id\",\"type\":\"uint256\"},{\"internalType\":\"string\",\"name\":\"title\",\"type\":\"string\"},{\"internalType\":\"string\",\"name\":\"description\",\"type\":\"string\"},{\"internalType\":\"bool\",\"name\":\"done\",\"type\":\"bool\"},{\"internalType\":\"uint256\",\"name\":\"createdAt\",\"type\":\"uint256\"}],\"stateMutability\":\"view\",\"type\":\"function\"},{\"inputs\":[{\"internalType\":\"uint256\",\"name\":\"_id\",\"type\":\"uint256\"}],\"name\":\"toggleDone\",\"outputs\":[],\"stateMutability\":\"nonpayable\",\"type\":\"function\"}],\"devdoc\":{\"kind\":\"dev\",\"methods\":{},\"version\":1},\"userdoc\":{\"kind\":\"user\",\"methods\":{},\"version\":1}},\"settings\":{\"compilationTarget\":{\"project:/contracts/TasksContract.sol\":\"TasksContract\"},\"evmVersion\":\"istanbul\",\"libraries\":{},\"metadata\":{\"bytecodeHash\":\"ipfs\"},\"optimizer\":{\"enabled\":false,\"runs\":200},\"remappings\":[]},\"sources\":{\"project:/contracts/TasksContract.sol\":{\"keccak256\":\"0xbced61127d5c738bb973d6fa7a5e66c3c7aa64eb91af7a4611d614e994792f93\",\"license\":\"MIT\",\"urls\":[\"bzz-raw://4d27e6b34f4e4d2e5f717f9d40317519685faf3a2f9d9af0b4e7ce2474773c4d\",\"dweb:/ipfs/QmbDjginE6kNpxoGqvrJjshGBxKvs3tn1Rgj3JNnTbNA7B\"]}},\"version\":1}",
  "bytecode": "0x6080604052600080553480156200001557600080fd5b50620000926040518060400160405280600a81526020017f5461736b732044417070000000000000000000000000000000000000000000008152506040518060400160405280601381526020017f506f7274656420746f20506f6c796a75696365000000000000000000000000008152506200009860201b60201c565b62000487565b600080815480929190620000ac90620003ca565b91905055506040518060a00160405280600054815260200183815260200182815260200160001515815260200142815250600160008054815260200190815260200160002060008201518160000155602082015181600101908051906020019062000119929190620001ae565b50604082015181600201908051906020019062000138929190620001ae565b5060608201518160030160006101000a81548160ff021916908315150217905550608082015181600401559050507f6549102bed7d1bb5ec529ee14e2ca60ffc1f47f66d4cc6ca713220613cc64c256000548383600042604051620001a2959493929190620002c1565b60405180910390a15050565b828054620001bc9062000394565b90600052602060002090601f016020900481019282620001e057600085556200022c565b82601f10620001fb57805160ff19168380011785556200022c565b828001600101855582156200022c579182015b828111156200022b5782518255916020019190600101906200020e565b5b5090506200023b91906200023f565b5090565b5b808211156200025a57600081600090555060010162000240565b5090565b620002698162000348565b82525050565b60006200027c826200032c565b62000288818562000337565b93506200029a8185602086016200035e565b620002a58162000476565b840191505092915050565b620002bb8162000354565b82525050565b600060a082019050620002d86000830188620002b0565b8181036020830152620002ec81876200026f565b905081810360408301526200030281866200026f565b90506200031360608301856200025e565b620003226080830184620002b0565b9695505050505050565b600081519050919050565b600082825260208201905092915050565b60008115159050919050565b6000819050919050565b60005b838110156200037e57808201518184015260208101905062000361565b838111156200038e576000848401525b50505050565b60006002820490506001821680620003ad57607f821691505b60208210811415620003c457620003c362000447565b5b50919050565b6000620003d78262000354565b91507fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff8214156200040d576200040c62000418565b5b600182019050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052602260045260246000fd5b6000601f19601f8301169050919050565b610a7e80620004976000396000f3fe608060405234801561001057600080fd5b506004361061004c5760003560e01c8063292a458514610051578063586717301461006d5780638d9776721461008b578063d81ef739146100bf575b600080fd5b61006b600480360381019061006691906106b2565b6100db565b005b6100756101e9565b604051610082919061079e565b60405180910390f35b6100a560048036038101906100a0919061071e565b6101ef565b6040516100b69594939291906107e2565b60405180910390f35b6100d960048036038101906100d4919061071e565b610342565b005b6000808154809291906100ed9061094a565b91905055506040518060a001604052806000548152602001838152602001828152602001600015158152602001428152506001600080548152602001908152602001600020600082015181600001556020820151816001019080519060200190610158929190610592565b506040820151816002019080519060200190610175929190610592565b5060608201518160030160006101000a81548160ff021916908315150217905550608082015181600401559050507f6549102bed7d1bb5ec529ee14e2ca60ffc1f47f66d4cc6ca713220613cc64c2560005483836000426040516101dd9594939291906107e2565b60405180910390a15050565b60005481565b600160205280600052604060002060009150905080600001549080600101805461021890610918565b80601f016020809104026020016040519081016040528092919081815260200182805461024490610918565b80156102915780601f1061026657610100808354040283529160200191610291565b820191906000526020600020905b81548152906001019060200180831161027457829003601f168201915b5050505050908060020180546102a690610918565b80601f01602080910402602001604051908101604052809291908181526020018280546102d290610918565b801561031f5780601f106102f45761010080835404028352916020019161031f565b820191906000526020600020905b81548152906001019060200180831161030257829003601f168201915b5050505050908060030160009054906101000a900460ff16908060040154905085565b6000600160008381526020019081526020016000206040518060a00160405290816000820154815260200160018201805461037c90610918565b80601f01602080910402602001604051908101604052809291908181526020018280546103a890610918565b80156103f55780601f106103ca576101008083540402835291602001916103f5565b820191906000526020600020905b8154815290600101906020018083116103d857829003601f168201915b5050505050815260200160028201805461040e90610918565b80601f016020809104026020016040519081016040528092919081815260200182805461043a90610918565b80156104875780601f1061045c57610100808354040283529160200191610487565b820191906000526020600020905b81548152906001019060200180831161046a57829003601f168201915b505050505081526020016003820160009054906101000a900460ff1615151515815260200160048201548152505090508060600151158160600190151590811515815250508060016000848152602001908152602001600020600082015181600001556020820151816001019080519060200190610506929190610592565b506040820151816002019080519060200190610523929190610592565b5060608201518160030160006101000a81548160ff021916908315150217905550608082015181600401559050507f3a359256e016dcfa8426ec503e08484999d6fcfb8c0f6084dc9e63374d8384298282606001516040516105869291906107b9565b60405180910390a15050565b82805461059e90610918565b90600052602060002090601f0160209004810192826105c05760008555610607565b82601f106105d957805160ff1916838001178555610607565b82800160010185558215610607579182015b828111156106065782518255916020019190600101906105eb565b5b5090506106149190610618565b5090565b5b80821115610631576000816000905550600101610619565b5090565b600061064861064384610874565b610843565b90508281526020810184848401111561066057600080fd5b61066b8482856108d6565b509392505050565b600082601f83011261068457600080fd5b8135610694848260208601610635565b91505092915050565b6000813590506106ac81610a31565b92915050565b600080604083850312156106c557600080fd5b600083013567ffffffffffffffff8111156106df57600080fd5b6106eb85828601610673565b925050602083013567ffffffffffffffff81111561070857600080fd5b61071485828601610673565b9150509250929050565b60006020828403121561073057600080fd5b600061073e8482850161069d565b91505092915050565b610750816108c0565b82525050565b6000610761826108a4565b61076b81856108af565b935061077b8185602086016108e5565b61078481610a20565b840191505092915050565b610798816108cc565b82525050565b60006020820190506107b3600083018461078f565b92915050565b60006040820190506107ce600083018561078f565b6107db6020830184610747565b9392505050565b600060a0820190506107f7600083018861078f565b81810360208301526108098187610756565b9050818103604083015261081d8186610756565b905061082c6060830185610747565b610839608083018461078f565b9695505050505050565b6000604051905081810181811067ffffffffffffffff8211171561086a576108696109f1565b5b8060405250919050565b600067ffffffffffffffff82111561088f5761088e6109f1565b5b601f19601f8301169050602081019050919050565b600081519050919050565b600082825260208201905092915050565b60008115159050919050565b6000819050919050565b82818337600083830152505050565b60005b838110156109035780820151818401526020810190506108e8565b83811115610912576000848401525b50505050565b6000600282049050600182168061093057607f821691505b60208210811415610944576109436109c2565b5b50919050565b6000610955826108cc565b91507fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff82141561098857610987610993565b5b600182019050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052602260045260246000fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052604160045260246000fd5b6000601f19601f8301169050919050565b610a3a816108cc565b8114610a4557600080fd5b5056fea2646970667358221220adc8da436ea618d1b09956087a2358cdfad0a770e30dc3abbe257a5a7113b15464736f6c63430008000033",
  "deployedBytecode": "0x608060405234801561001057600080fd5b506004361061004c5760003560e01c8063292a458514610051578063586717301461006d5780638d9776721461008b578063d81ef739146100bf575b600080fd5b61006b600480360381019061006691906106b2565b6100db565b005b6100756101e9565b604051610082919061079e565b60405180910390f35b6100a560048036038101906100a0919061071e565b6101ef565b6040516100b69594939291906107e2565b60405180910390f35b6100d960048036038101906100d4919061071e565b610342565b005b6000808154809291906100ed9061094a565b91905055506040518060a001604052806000548152602001838152602001828152602001600015158152602001428152506001600080548152602001908152602001600020600082015181600001556020820151816001019080519060200190610158929190610592565b506040820151816002019080519060200190610175929190610592565b5060608201518160030160006101000a81548160ff021916908315150217905550608082015181600401559050507f6549102bed7d1bb5ec529ee14e2ca60ffc1f47f66d4cc6ca713220613cc64c2560005483836000426040516101dd9594939291906107e2565b60405180910390a15050565b60005481565b600160205280600052604060002060009150905080600001549080600101805461021890610918565b80601f016020809104026020016040519081016040528092919081815260200182805461024490610918565b80156102915780601f1061026657610100808354040283529160200191610291565b820191906000526020600020905b81548152906001019060200180831161027457829003601f168201915b5050505050908060020180546102a690610918565b80601f01602080910402602001604051908101604052809291908181526020018280546102d290610918565b801561031f5780601f106102f45761010080835404028352916020019161031f565b820191906000526020600020905b81548152906001019060200180831161030257829003601f168201915b5050505050908060030160009054906101000a900460ff16908060040154905085565b6000600160008381526020019081526020016000206040518060a00160405290816000820154815260200160018201805461037c90610918565b80601f01602080910402602001604051908101604052809291908181526020018280546103a890610918565b80156103f55780601f106103ca576101008083540402835291602001916103f5565b820191906000526020600020905b8154815290600101906020018083116103d857829003601f168201915b5050505050815260200160028201805461040e90610918565b80601f016020809104026020016040519081016040528092919081815260200182805461043a90610918565b80156104875780601f1061045c57610100808354040283529160200191610487565b820191906000526020600020905b81548152906001019060200180831161046a57829003601f168201915b505050505081526020016003820160009054906101000a900460ff1615151515815260200160048201548152505090508060600151158160600190151590811515815250508060016000848152602001908152602001600020600082015181600001556020820151816001019080519060200190610506929190610592565b506040820151816002019080519060200190610523929190610592565b5060608201518160030160006101000a81548160ff021916908315150217905550608082015181600401559050507f3a359256e016dcfa8426ec503e08484999d6fcfb8c0f6084dc9e63374d8384298282606001516040516105869291906107b9565b60405180910390a15050565b82805461059e90610918565b90600052602060002090601f0160209004810192826105c05760008555610607565b82601f106105d957805160ff1916838001178555610607565b82800160010185558215610607579182015b828111156106065782518255916020019190600101906105eb565b5b5090506106149190610618565b5090565b5b80821115610631576000816000905550600101610619565b5090565b600061064861064384610874565b610843565b90508281526020810184848401111561066057600080fd5b61066b8482856108d6565b509392505050565b600082601f83011261068457600080fd5b8135610694848260208601610635565b91505092915050565b6000813590506106ac81610a31565b92915050565b600080604083850312156106c557600080fd5b600083013567ffffffffffffffff8111156106df57600080fd5b6106eb85828601610673565b925050602083013567ffffffffffffffff81111561070857600080fd5b61071485828601610673565b9150509250929050565b60006020828403121561073057600080fd5b600061073e8482850161069d565b91505092915050565b610750816108c0565b82525050565b6000610761826108a4565b61076b81856108af565b935061077b8185602086016108e5565b61078481610a20565b840191505092915050565b610798816108cc565b82525050565b60006020820190506107b3600083018461078f565b92915050565b60006040820190506107ce600083018561078f565b6107db6020830184610747565b9392505050565b600060a0820190506107f7600083018861078f565b81810360208301526108098187610756565b9050818103604083015261081d8186610756565b905061082c6060830185610747565b610839608083018461078f565b9695505050505050565b6000604051905081810181811067ffffffffffffffff8211171561086a576108696109f1565b5b8060405250919050565b600067ffffffffffffffff82111561088f5761088e6109f1565b5b601f19601f8301169050602081019050919050565b600081519050919050565b600082825260208201905092915050565b60008115159050919050565b6000819050919050565b82818337600083830152505050565b60005b838110156109035780820151818401526020810190506108e8565b83811115610912576000848401525b50505050565b6000600282049050600182168061093057607f821691505b60208210811415610944576109436109c2565b5b50919050565b6000610955826108cc565b91507fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff82141561098857610987610993565b5b600182019050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052602260045260246000fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052604160045260246000fd5b6000601f19601f8301169050919050565b610a3a816108cc565b8114610a4557600080fd5b5056fea2646970667358221220adc8da436ea618d1b09956087a2358cdfad0a770e30dc3abbe257a5a7113b15464736f6c63430008000033",
  "immutableReferences": {},
  "generatedSources": [
    {
      "ast": {
        "nodeType": "YulBlock",
        "src": "0:3270:1",
        "statements": [
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "66:50:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "83:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "103:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "cleanup_t_bool",
                          "nodeType": "YulIdentifier",
                          "src": "88:14:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "88:21:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "76:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "76:34:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "76:34:1"
                }
              ]
            },
            "name": "abi_encode_t_bool_to_t_bool_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "54:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "61:3:1",
                "type": ""
              }
            ],
            "src": "7:109:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "214:272:1",
              "statements": [
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "224:53:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "271:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "array_length_t_string_memory_ptr",
                      "nodeType": "YulIdentifier",
                      "src": "238:32:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "238:39:1"
                  },
                  "variables": [
                    {
                      "name": "length",
                      "nodeType": "YulTypedName",
                      "src": "228:6:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "286:78:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "352:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "357:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "array_storeLengthForEncoding_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "293:58:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "293:71:1"
                  },
                  "variableNames": [
                    {
                      "name": "pos",
                      "nodeType": "YulIdentifier",
                      "src": "286:3:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "399:5:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "406:4:1",
                            "type": "",
                            "value": "0x20"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "395:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "395:16:1"
                      },
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "413:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "418:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "copy_memory_to_memory",
                      "nodeType": "YulIdentifier",
                      "src": "373:21:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "373:52:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "373:52:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "434:46:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "445:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "472:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "round_up_to_mul_of_32",
                          "nodeType": "YulIdentifier",
                          "src": "450:21:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "450:29:1"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "441:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "441:39:1"
                  },
                  "variableNames": [
                    {
                      "name": "end",
                      "nodeType": "YulIdentifier",
                      "src": "434:3:1"
                    }
                  ]
                }
              ]
            },
            "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "195:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "202:3:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "end",
                "nodeType": "YulTypedName",
                "src": "210:3:1",
                "type": ""
              }
            ],
            "src": "122:364:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "557:53:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "574:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "597:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "cleanup_t_uint256",
                          "nodeType": "YulIdentifier",
                          "src": "579:17:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "579:24:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "567:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "567:37:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "567:37:1"
                }
              ]
            },
            "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "545:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "552:3:1",
                "type": ""
              }
            ],
            "src": "492:118:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "860:590:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "870:27:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "headStart",
                        "nodeType": "YulIdentifier",
                        "src": "882:9:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "893:3:1",
                        "type": "",
                        "value": "160"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "878:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "878:19:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "870:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value0",
                        "nodeType": "YulIdentifier",
                        "src": "951:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "964:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "975:1:1",
                            "type": "",
                            "value": "0"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "960:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "960:17:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "907:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "907:71:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "907:71:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "999:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1010:2:1",
                            "type": "",
                            "value": "32"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "995:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "995:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "tail",
                            "nodeType": "YulIdentifier",
                            "src": "1019:4:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1025:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "1015:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1015:20:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "988:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "988:48:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "988:48:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "1045:86:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value1",
                        "nodeType": "YulIdentifier",
                        "src": "1117:6:1"
                      },
                      {
                        "name": "tail",
                        "nodeType": "YulIdentifier",
                        "src": "1126:4:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "1053:63:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1053:78:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "1045:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1152:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1163:2:1",
                            "type": "",
                            "value": "64"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "1148:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1148:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "tail",
                            "nodeType": "YulIdentifier",
                            "src": "1172:4:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1178:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "1168:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1168:20:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "1141:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1141:48:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "1141:48:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "1198:86:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value2",
                        "nodeType": "YulIdentifier",
                        "src": "1270:6:1"
                      },
                      {
                        "name": "tail",
                        "nodeType": "YulIdentifier",
                        "src": "1279:4:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "1206:63:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1206:78:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "1198:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value3",
                        "nodeType": "YulIdentifier",
                        "src": "1332:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1345:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1356:2:1",
                            "type": "",
                            "value": "96"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "1341:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1341:18:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_bool_to_t_bool_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "1294:37:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1294:66:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "1294:66:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value4",
                        "nodeType": "YulIdentifier",
                        "src": "1414:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1427:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1438:3:1",
                            "type": "",
                            "value": "128"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "1423:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1423:19:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "1370:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1370:73:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "1370:73:1"
                }
              ]
            },
            "name": "abi_encode_tuple_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__to_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__fromStack_reversed",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "800:9:1",
                "type": ""
              },
              {
                "name": "value4",
                "nodeType": "YulTypedName",
                "src": "812:6:1",
                "type": ""
              },
              {
                "name": "value3",
                "nodeType": "YulTypedName",
                "src": "820:6:1",
                "type": ""
              },
              {
                "name": "value2",
                "nodeType": "YulTypedName",
                "src": "828:6:1",
                "type": ""
              },
              {
                "name": "value1",
                "nodeType": "YulTypedName",
                "src": "836:6:1",
                "type": ""
              },
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "844:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "tail",
                "nodeType": "YulTypedName",
                "src": "855:4:1",
                "type": ""
              }
            ],
            "src": "616:834:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1515:40:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "1526:22:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "1542:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "mload",
                      "nodeType": "YulIdentifier",
                      "src": "1536:5:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1536:12:1"
                  },
                  "variableNames": [
                    {
                      "name": "length",
                      "nodeType": "YulIdentifier",
                      "src": "1526:6:1"
                    }
                  ]
                }
              ]
            },
            "name": "array_length_t_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "1498:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "1508:6:1",
                "type": ""
              }
            ],
            "src": "1456:99:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1657:73:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "1674:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "1679:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "1667:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1667:19:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "1667:19:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "1695:29:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "1714:3:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "1719:4:1",
                        "type": "",
                        "value": "0x20"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "1710:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1710:14:1"
                  },
                  "variableNames": [
                    {
                      "name": "updated_pos",
                      "nodeType": "YulIdentifier",
                      "src": "1695:11:1"
                    }
                  ]
                }
              ]
            },
            "name": "array_storeLengthForEncoding_t_string_memory_ptr_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "1629:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "1634:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "updated_pos",
                "nodeType": "YulTypedName",
                "src": "1645:11:1",
                "type": ""
              }
            ],
            "src": "1561:169:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1778:48:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "1788:32:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "1813:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "iszero",
                          "nodeType": "YulIdentifier",
                          "src": "1806:6:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1806:13:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "1799:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1799:21:1"
                  },
                  "variableNames": [
                    {
                      "name": "cleaned",
                      "nodeType": "YulIdentifier",
                      "src": "1788:7:1"
                    }
                  ]
                }
              ]
            },
            "name": "cleanup_t_bool",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "1760:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "cleaned",
                "nodeType": "YulTypedName",
                "src": "1770:7:1",
                "type": ""
              }
            ],
            "src": "1736:90:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1877:32:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "1887:16:1",
                  "value": {
                    "name": "value",
                    "nodeType": "YulIdentifier",
                    "src": "1898:5:1"
                  },
                  "variableNames": [
                    {
                      "name": "cleaned",
                      "nodeType": "YulIdentifier",
                      "src": "1887:7:1"
                    }
                  ]
                }
              ]
            },
            "name": "cleanup_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "1859:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "cleaned",
                "nodeType": "YulTypedName",
                "src": "1869:7:1",
                "type": ""
              }
            ],
            "src": "1832:77:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1964:258:1",
              "statements": [
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "1974:10:1",
                  "value": {
                    "kind": "number",
                    "nodeType": "YulLiteral",
                    "src": "1983:1:1",
                    "type": "",
                    "value": "0"
                  },
                  "variables": [
                    {
                      "name": "i",
                      "nodeType": "YulTypedName",
                      "src": "1978:1:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "2043:63:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "arguments": [
                                {
                                  "name": "dst",
                                  "nodeType": "YulIdentifier",
                                  "src": "2068:3:1"
                                },
                                {
                                  "name": "i",
                                  "nodeType": "YulIdentifier",
                                  "src": "2073:1:1"
                                }
                              ],
                              "functionName": {
                                "name": "add",
                                "nodeType": "YulIdentifier",
                                "src": "2064:3:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "2064:11:1"
                            },
                            {
                              "arguments": [
                                {
                                  "arguments": [
                                    {
                                      "name": "src",
                                      "nodeType": "YulIdentifier",
                                      "src": "2087:3:1"
                                    },
                                    {
                                      "name": "i",
                                      "nodeType": "YulIdentifier",
                                      "src": "2092:1:1"
                                    }
                                  ],
                                  "functionName": {
                                    "name": "add",
                                    "nodeType": "YulIdentifier",
                                    "src": "2083:3:1"
                                  },
                                  "nodeType": "YulFunctionCall",
                                  "src": "2083:11:1"
                                }
                              ],
                              "functionName": {
                                "name": "mload",
                                "nodeType": "YulIdentifier",
                                "src": "2077:5:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "2077:18:1"
                            }
                          ],
                          "functionName": {
                            "name": "mstore",
                            "nodeType": "YulIdentifier",
                            "src": "2057:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2057:39:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "2057:39:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "i",
                        "nodeType": "YulIdentifier",
                        "src": "2004:1:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "2007:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "lt",
                      "nodeType": "YulIdentifier",
                      "src": "2001:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2001:13:1"
                  },
                  "nodeType": "YulForLoop",
                  "post": {
                    "nodeType": "YulBlock",
                    "src": "2015:19:1",
                    "statements": [
                      {
                        "nodeType": "YulAssignment",
                        "src": "2017:15:1",
                        "value": {
                          "arguments": [
                            {
                              "name": "i",
                              "nodeType": "YulIdentifier",
                              "src": "2026:1:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "2029:2:1",
                              "type": "",
                              "value": "32"
                            }
                          ],
                          "functionName": {
                            "name": "add",
                            "nodeType": "YulIdentifier",
                            "src": "2022:3:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2022:10:1"
                        },
                        "variableNames": [
                          {
                            "name": "i",
                            "nodeType": "YulIdentifier",
                            "src": "2017:1:1"
                          }
                        ]
                      }
                    ]
                  },
                  "pre": {
                    "nodeType": "YulBlock",
                    "src": "1997:3:1",
                    "statements": []
                  },
                  "src": "1993:113:1"
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "2140:76:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "arguments": [
                                {
                                  "name": "dst",
                                  "nodeType": "YulIdentifier",
                                  "src": "2190:3:1"
                                },
                                {
                                  "name": "length",
                                  "nodeType": "YulIdentifier",
                                  "src": "2195:6:1"
                                }
                              ],
                              "functionName": {
                                "name": "add",
                                "nodeType": "YulIdentifier",
                                "src": "2186:3:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "2186:16:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "2204:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "mstore",
                            "nodeType": "YulIdentifier",
                            "src": "2179:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2179:27:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "2179:27:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "i",
                        "nodeType": "YulIdentifier",
                        "src": "2121:1:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "2124:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "gt",
                      "nodeType": "YulIdentifier",
                      "src": "2118:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2118:13:1"
                  },
                  "nodeType": "YulIf",
                  "src": "2115:2:1"
                }
              ]
            },
            "name": "copy_memory_to_memory",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "src",
                "nodeType": "YulTypedName",
                "src": "1946:3:1",
                "type": ""
              },
              {
                "name": "dst",
                "nodeType": "YulTypedName",
                "src": "1951:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "1956:6:1",
                "type": ""
              }
            ],
            "src": "1915:307:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2279:269:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "2289:22:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "data",
                        "nodeType": "YulIdentifier",
                        "src": "2303:4:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2309:1:1",
                        "type": "",
                        "value": "2"
                      }
                    ],
                    "functionName": {
                      "name": "div",
                      "nodeType": "YulIdentifier",
                      "src": "2299:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2299:12:1"
                  },
                  "variableNames": [
                    {
                      "name": "length",
                      "nodeType": "YulIdentifier",
                      "src": "2289:6:1"
                    }
                  ]
                },
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "2320:38:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "data",
                        "nodeType": "YulIdentifier",
                        "src": "2350:4:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2356:1:1",
                        "type": "",
                        "value": "1"
                      }
                    ],
                    "functionName": {
                      "name": "and",
                      "nodeType": "YulIdentifier",
                      "src": "2346:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2346:12:1"
                  },
                  "variables": [
                    {
                      "name": "outOfPlaceEncoding",
                      "nodeType": "YulTypedName",
                      "src": "2324:18:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "2397:51:1",
                    "statements": [
                      {
                        "nodeType": "YulAssignment",
                        "src": "2411:27:1",
                        "value": {
                          "arguments": [
                            {
                              "name": "length",
                              "nodeType": "YulIdentifier",
                              "src": "2425:6:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "2433:4:1",
                              "type": "",
                              "value": "0x7f"
                            }
                          ],
                          "functionName": {
                            "name": "and",
                            "nodeType": "YulIdentifier",
                            "src": "2421:3:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2421:17:1"
                        },
                        "variableNames": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "2411:6:1"
                          }
                        ]
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "outOfPlaceEncoding",
                        "nodeType": "YulIdentifier",
                        "src": "2377:18:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "2370:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2370:26:1"
                  },
                  "nodeType": "YulIf",
                  "src": "2367:2:1"
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "2500:42:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x22",
                            "nodeType": "YulIdentifier",
                            "src": "2514:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2514:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "2514:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "outOfPlaceEncoding",
                        "nodeType": "YulIdentifier",
                        "src": "2464:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "2487:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "2495:2:1",
                            "type": "",
                            "value": "32"
                          }
                        ],
                        "functionName": {
                          "name": "lt",
                          "nodeType": "YulIdentifier",
                          "src": "2484:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2484:14:1"
                      }
                    ],
                    "functionName": {
                      "name": "eq",
                      "nodeType": "YulIdentifier",
                      "src": "2461:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2461:38:1"
                  },
                  "nodeType": "YulIf",
                  "src": "2458:2:1"
                }
              ]
            },
            "name": "extract_byte_array_length",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "data",
                "nodeType": "YulTypedName",
                "src": "2263:4:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "2272:6:1",
                "type": ""
              }
            ],
            "src": "2228:320:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2597:190:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "2607:33:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "2634:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "cleanup_t_uint256",
                      "nodeType": "YulIdentifier",
                      "src": "2616:17:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2616:24:1"
                  },
                  "variableNames": [
                    {
                      "name": "value",
                      "nodeType": "YulIdentifier",
                      "src": "2607:5:1"
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "2730:22:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x11",
                            "nodeType": "YulIdentifier",
                            "src": "2732:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "2732:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "2732:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "2655:5:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2662:66:1",
                        "type": "",
                        "value": "0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff"
                      }
                    ],
                    "functionName": {
                      "name": "eq",
                      "nodeType": "YulIdentifier",
                      "src": "2652:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2652:77:1"
                  },
                  "nodeType": "YulIf",
                  "src": "2649:2:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "2761:20:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "2772:5:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2779:1:1",
                        "type": "",
                        "value": "1"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "2768:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2768:13:1"
                  },
                  "variableNames": [
                    {
                      "name": "ret",
                      "nodeType": "YulIdentifier",
                      "src": "2761:3:1"
                    }
                  ]
                }
              ]
            },
            "name": "increment_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "2583:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "ret",
                "nodeType": "YulTypedName",
                "src": "2593:3:1",
                "type": ""
              }
            ],
            "src": "2554:233:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2821:152:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2838:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2841:77:1",
                        "type": "",
                        "value": "35408467139433450592217433187231851964531694900788300625387963629091585785856"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "2831:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2831:88:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2831:88:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2935:1:1",
                        "type": "",
                        "value": "4"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2938:4:1",
                        "type": "",
                        "value": "0x11"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "2928:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2928:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2928:15:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2959:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2962:4:1",
                        "type": "",
                        "value": "0x24"
                      }
                    ],
                    "functionName": {
                      "name": "revert",
                      "nodeType": "YulIdentifier",
                      "src": "2952:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2952:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2952:15:1"
                }
              ]
            },
            "name": "panic_error_0x11",
            "nodeType": "YulFunctionDefinition",
            "src": "2793:180:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "3007:152:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3024:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3027:77:1",
                        "type": "",
                        "value": "35408467139433450592217433187231851964531694900788300625387963629091585785856"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "3017:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3017:88:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3017:88:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3121:1:1",
                        "type": "",
                        "value": "4"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3124:4:1",
                        "type": "",
                        "value": "0x22"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "3114:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3114:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3114:15:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3145:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3148:4:1",
                        "type": "",
                        "value": "0x24"
                      }
                    ],
                    "functionName": {
                      "name": "revert",
                      "nodeType": "YulIdentifier",
                      "src": "3138:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3138:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3138:15:1"
                }
              ]
            },
            "name": "panic_error_0x22",
            "nodeType": "YulFunctionDefinition",
            "src": "2979:180:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "3213:54:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "3223:38:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "3241:5:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3248:2:1",
                            "type": "",
                            "value": "31"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3237:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3237:14:1"
                      },
                      {
                        "arguments": [
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3257:2:1",
                            "type": "",
                            "value": "31"
                          }
                        ],
                        "functionName": {
                          "name": "not",
                          "nodeType": "YulIdentifier",
                          "src": "3253:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3253:7:1"
                      }
                    ],
                    "functionName": {
                      "name": "and",
                      "nodeType": "YulIdentifier",
                      "src": "3233:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3233:28:1"
                  },
                  "variableNames": [
                    {
                      "name": "result",
                      "nodeType": "YulIdentifier",
                      "src": "3223:6:1"
                    }
                  ]
                }
              ]
            },
            "name": "round_up_to_mul_of_32",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "3196:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "result",
                "nodeType": "YulTypedName",
                "src": "3206:6:1",
                "type": ""
              }
            ],
            "src": "3165:102:1"
          }
        ]
      },
      "contents": "{\n\n    function abi_encode_t_bool_to_t_bool_fromStack(value, pos) {\n        mstore(pos, cleanup_t_bool(value))\n    }\n\n    function abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value, pos) -> end {\n        let length := array_length_t_string_memory_ptr(value)\n        pos := array_storeLengthForEncoding_t_string_memory_ptr_fromStack(pos, length)\n        copy_memory_to_memory(add(value, 0x20), pos, length)\n        end := add(pos, round_up_to_mul_of_32(length))\n    }\n\n    function abi_encode_t_uint256_to_t_uint256_fromStack(value, pos) {\n        mstore(pos, cleanup_t_uint256(value))\n    }\n\n    function abi_encode_tuple_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__to_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__fromStack_reversed(headStart , value4, value3, value2, value1, value0) -> tail {\n        tail := add(headStart, 160)\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value0,  add(headStart, 0))\n\n        mstore(add(headStart, 32), sub(tail, headStart))\n        tail := abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value1,  tail)\n\n        mstore(add(headStart, 64), sub(tail, headStart))\n        tail := abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value2,  tail)\n\n        abi_encode_t_bool_to_t_bool_fromStack(value3,  add(headStart, 96))\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value4,  add(headStart, 128))\n\n    }\n\n    function array_length_t_string_memory_ptr(value) -> length {\n\n        length := mload(value)\n\n    }\n\n    function array_storeLengthForEncoding_t_string_memory_ptr_fromStack(pos, length) -> updated_pos {\n        mstore(pos, length)\n        updated_pos := add(pos, 0x20)\n    }\n\n    function cleanup_t_bool(value) -> cleaned {\n        cleaned := iszero(iszero(value))\n    }\n\n    function cleanup_t_uint256(value) -> cleaned {\n        cleaned := value\n    }\n\n    function copy_memory_to_memory(src, dst, length) {\n        let i := 0\n        for { } lt(i, length) { i := add(i, 32) }\n        {\n            mstore(add(dst, i), mload(add(src, i)))\n        }\n        if gt(i, length)\n        {\n            // clear end\n            mstore(add(dst, length), 0)\n        }\n    }\n\n    function extract_byte_array_length(data) -> length {\n        length := div(data, 2)\n        let outOfPlaceEncoding := and(data, 1)\n        if iszero(outOfPlaceEncoding) {\n            length := and(length, 0x7f)\n        }\n\n        if eq(outOfPlaceEncoding, lt(length, 32)) {\n            panic_error_0x22()\n        }\n    }\n\n    function increment_t_uint256(value) -> ret {\n        value := cleanup_t_uint256(value)\n        if eq(value, 0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff) { panic_error_0x11() }\n        ret := add(value, 1)\n    }\n\n    function panic_error_0x11() {\n        mstore(0, 35408467139433450592217433187231851964531694900788300625387963629091585785856)\n        mstore(4, 0x11)\n        revert(0, 0x24)\n    }\n\n    function panic_error_0x22() {\n        mstore(0, 35408467139433450592217433187231851964531694900788300625387963629091585785856)\n        mstore(4, 0x22)\n        revert(0, 0x24)\n    }\n\n    function round_up_to_mul_of_32(value) -> result {\n        result := and(add(value, 31), not(31))\n    }\n\n}\n",
      "id": 1,
      "language": "Yul",
      "name": "#utility.yul"
    }
  ],
  "deployedGeneratedSources": [
    {
      "ast": {
        "nodeType": "YulBlock",
        "src": "0:6620:1",
        "statements": [
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "91:260:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "101:74:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "167:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "array_allocation_size_t_string_memory_ptr",
                          "nodeType": "YulIdentifier",
                          "src": "125:41:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "125:49:1"
                      }
                    ],
                    "functionName": {
                      "name": "allocateMemory",
                      "nodeType": "YulIdentifier",
                      "src": "110:14:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "110:65:1"
                  },
                  "variableNames": [
                    {
                      "name": "array",
                      "nodeType": "YulIdentifier",
                      "src": "101:5:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "array",
                        "nodeType": "YulIdentifier",
                        "src": "191:5:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "198:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "184:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "184:21:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "184:21:1"
                },
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "214:27:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "array",
                        "nodeType": "YulIdentifier",
                        "src": "229:5:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "236:4:1",
                        "type": "",
                        "value": "0x20"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "225:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "225:16:1"
                  },
                  "variables": [
                    {
                      "name": "dst",
                      "nodeType": "YulTypedName",
                      "src": "218:3:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "279:16:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "288:1:1",
                              "type": "",
                              "value": "0"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "291:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "revert",
                            "nodeType": "YulIdentifier",
                            "src": "281:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "281:12:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "281:12:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "src",
                            "nodeType": "YulIdentifier",
                            "src": "260:3:1"
                          },
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "265:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "256:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "256:16:1"
                      },
                      {
                        "name": "end",
                        "nodeType": "YulIdentifier",
                        "src": "274:3:1"
                      }
                    ],
                    "functionName": {
                      "name": "gt",
                      "nodeType": "YulIdentifier",
                      "src": "253:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "253:25:1"
                  },
                  "nodeType": "YulIf",
                  "src": "250:2:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "src",
                        "nodeType": "YulIdentifier",
                        "src": "328:3:1"
                      },
                      {
                        "name": "dst",
                        "nodeType": "YulIdentifier",
                        "src": "333:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "338:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "copy_calldata_to_memory",
                      "nodeType": "YulIdentifier",
                      "src": "304:23:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "304:41:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "304:41:1"
                }
              ]
            },
            "name": "abi_decode_available_length_t_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "src",
                "nodeType": "YulTypedName",
                "src": "64:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "69:6:1",
                "type": ""
              },
              {
                "name": "end",
                "nodeType": "YulTypedName",
                "src": "77:3:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "array",
                "nodeType": "YulTypedName",
                "src": "85:5:1",
                "type": ""
              }
            ],
            "src": "7:344:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "433:211:1",
              "statements": [
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "482:16:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "491:1:1",
                              "type": "",
                              "value": "0"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "494:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "revert",
                            "nodeType": "YulIdentifier",
                            "src": "484:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "484:12:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "484:12:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "offset",
                                "nodeType": "YulIdentifier",
                                "src": "461:6:1"
                              },
                              {
                                "kind": "number",
                                "nodeType": "YulLiteral",
                                "src": "469:4:1",
                                "type": "",
                                "value": "0x1f"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "457:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "457:17:1"
                          },
                          {
                            "name": "end",
                            "nodeType": "YulIdentifier",
                            "src": "476:3:1"
                          }
                        ],
                        "functionName": {
                          "name": "slt",
                          "nodeType": "YulIdentifier",
                          "src": "453:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "453:27:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "446:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "446:35:1"
                  },
                  "nodeType": "YulIf",
                  "src": "443:2:1"
                },
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "507:34:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "offset",
                        "nodeType": "YulIdentifier",
                        "src": "534:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "calldataload",
                      "nodeType": "YulIdentifier",
                      "src": "521:12:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "521:20:1"
                  },
                  "variables": [
                    {
                      "name": "length",
                      "nodeType": "YulTypedName",
                      "src": "511:6:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "550:88:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "offset",
                            "nodeType": "YulIdentifier",
                            "src": "611:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "619:4:1",
                            "type": "",
                            "value": "0x20"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "607:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "607:17:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "626:6:1"
                      },
                      {
                        "name": "end",
                        "nodeType": "YulIdentifier",
                        "src": "634:3:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_decode_available_length_t_string_memory_ptr",
                      "nodeType": "YulIdentifier",
                      "src": "559:47:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "559:79:1"
                  },
                  "variableNames": [
                    {
                      "name": "array",
                      "nodeType": "YulIdentifier",
                      "src": "550:5:1"
                    }
                  ]
                }
              ]
            },
            "name": "abi_decode_t_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "offset",
                "nodeType": "YulTypedName",
                "src": "411:6:1",
                "type": ""
              },
              {
                "name": "end",
                "nodeType": "YulTypedName",
                "src": "419:3:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "array",
                "nodeType": "YulTypedName",
                "src": "427:5:1",
                "type": ""
              }
            ],
            "src": "371:273:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "702:87:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "712:29:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "offset",
                        "nodeType": "YulIdentifier",
                        "src": "734:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "calldataload",
                      "nodeType": "YulIdentifier",
                      "src": "721:12:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "721:20:1"
                  },
                  "variableNames": [
                    {
                      "name": "value",
                      "nodeType": "YulIdentifier",
                      "src": "712:5:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "777:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "validator_revert_t_uint256",
                      "nodeType": "YulIdentifier",
                      "src": "750:26:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "750:33:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "750:33:1"
                }
              ]
            },
            "name": "abi_decode_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "offset",
                "nodeType": "YulTypedName",
                "src": "680:6:1",
                "type": ""
              },
              {
                "name": "end",
                "nodeType": "YulTypedName",
                "src": "688:3:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "696:5:1",
                "type": ""
              }
            ],
            "src": "650:139:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "898:530:1",
              "statements": [
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "944:16:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "953:1:1",
                              "type": "",
                              "value": "0"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "956:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "revert",
                            "nodeType": "YulIdentifier",
                            "src": "946:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "946:12:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "946:12:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "dataEnd",
                            "nodeType": "YulIdentifier",
                            "src": "919:7:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "928:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "915:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "915:23:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "940:2:1",
                        "type": "",
                        "value": "64"
                      }
                    ],
                    "functionName": {
                      "name": "slt",
                      "nodeType": "YulIdentifier",
                      "src": "911:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "911:32:1"
                  },
                  "nodeType": "YulIf",
                  "src": "908:2:1"
                },
                {
                  "nodeType": "YulBlock",
                  "src": "970:220:1",
                  "statements": [
                    {
                      "nodeType": "YulVariableDeclaration",
                      "src": "985:45:1",
                      "value": {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "headStart",
                                "nodeType": "YulIdentifier",
                                "src": "1016:9:1"
                              },
                              {
                                "kind": "number",
                                "nodeType": "YulLiteral",
                                "src": "1027:1:1",
                                "type": "",
                                "value": "0"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "1012:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "1012:17:1"
                          }
                        ],
                        "functionName": {
                          "name": "calldataload",
                          "nodeType": "YulIdentifier",
                          "src": "999:12:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "999:31:1"
                      },
                      "variables": [
                        {
                          "name": "offset",
                          "nodeType": "YulTypedName",
                          "src": "989:6:1",
                          "type": ""
                        }
                      ]
                    },
                    {
                      "body": {
                        "nodeType": "YulBlock",
                        "src": "1077:16:1",
                        "statements": [
                          {
                            "expression": {
                              "arguments": [
                                {
                                  "kind": "number",
                                  "nodeType": "YulLiteral",
                                  "src": "1086:1:1",
                                  "type": "",
                                  "value": "0"
                                },
                                {
                                  "kind": "number",
                                  "nodeType": "YulLiteral",
                                  "src": "1089:1:1",
                                  "type": "",
                                  "value": "0"
                                }
                              ],
                              "functionName": {
                                "name": "revert",
                                "nodeType": "YulIdentifier",
                                "src": "1079:6:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "1079:12:1"
                            },
                            "nodeType": "YulExpressionStatement",
                            "src": "1079:12:1"
                          }
                        ]
                      },
                      "condition": {
                        "arguments": [
                          {
                            "name": "offset",
                            "nodeType": "YulIdentifier",
                            "src": "1049:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1057:18:1",
                            "type": "",
                            "value": "0xffffffffffffffff"
                          }
                        ],
                        "functionName": {
                          "name": "gt",
                          "nodeType": "YulIdentifier",
                          "src": "1046:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1046:30:1"
                      },
                      "nodeType": "YulIf",
                      "src": "1043:2:1"
                    },
                    {
                      "nodeType": "YulAssignment",
                      "src": "1107:73:1",
                      "value": {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "headStart",
                                "nodeType": "YulIdentifier",
                                "src": "1152:9:1"
                              },
                              {
                                "name": "offset",
                                "nodeType": "YulIdentifier",
                                "src": "1163:6:1"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "1148:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "1148:22:1"
                          },
                          {
                            "name": "dataEnd",
                            "nodeType": "YulIdentifier",
                            "src": "1172:7:1"
                          }
                        ],
                        "functionName": {
                          "name": "abi_decode_t_string_memory_ptr",
                          "nodeType": "YulIdentifier",
                          "src": "1117:30:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1117:63:1"
                      },
                      "variableNames": [
                        {
                          "name": "value0",
                          "nodeType": "YulIdentifier",
                          "src": "1107:6:1"
                        }
                      ]
                    }
                  ]
                },
                {
                  "nodeType": "YulBlock",
                  "src": "1200:221:1",
                  "statements": [
                    {
                      "nodeType": "YulVariableDeclaration",
                      "src": "1215:46:1",
                      "value": {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "headStart",
                                "nodeType": "YulIdentifier",
                                "src": "1246:9:1"
                              },
                              {
                                "kind": "number",
                                "nodeType": "YulLiteral",
                                "src": "1257:2:1",
                                "type": "",
                                "value": "32"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "1242:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "1242:18:1"
                          }
                        ],
                        "functionName": {
                          "name": "calldataload",
                          "nodeType": "YulIdentifier",
                          "src": "1229:12:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1229:32:1"
                      },
                      "variables": [
                        {
                          "name": "offset",
                          "nodeType": "YulTypedName",
                          "src": "1219:6:1",
                          "type": ""
                        }
                      ]
                    },
                    {
                      "body": {
                        "nodeType": "YulBlock",
                        "src": "1308:16:1",
                        "statements": [
                          {
                            "expression": {
                              "arguments": [
                                {
                                  "kind": "number",
                                  "nodeType": "YulLiteral",
                                  "src": "1317:1:1",
                                  "type": "",
                                  "value": "0"
                                },
                                {
                                  "kind": "number",
                                  "nodeType": "YulLiteral",
                                  "src": "1320:1:1",
                                  "type": "",
                                  "value": "0"
                                }
                              ],
                              "functionName": {
                                "name": "revert",
                                "nodeType": "YulIdentifier",
                                "src": "1310:6:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "1310:12:1"
                            },
                            "nodeType": "YulExpressionStatement",
                            "src": "1310:12:1"
                          }
                        ]
                      },
                      "condition": {
                        "arguments": [
                          {
                            "name": "offset",
                            "nodeType": "YulIdentifier",
                            "src": "1280:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "1288:18:1",
                            "type": "",
                            "value": "0xffffffffffffffff"
                          }
                        ],
                        "functionName": {
                          "name": "gt",
                          "nodeType": "YulIdentifier",
                          "src": "1277:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1277:30:1"
                      },
                      "nodeType": "YulIf",
                      "src": "1274:2:1"
                    },
                    {
                      "nodeType": "YulAssignment",
                      "src": "1338:73:1",
                      "value": {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "headStart",
                                "nodeType": "YulIdentifier",
                                "src": "1383:9:1"
                              },
                              {
                                "name": "offset",
                                "nodeType": "YulIdentifier",
                                "src": "1394:6:1"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "1379:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "1379:22:1"
                          },
                          {
                            "name": "dataEnd",
                            "nodeType": "YulIdentifier",
                            "src": "1403:7:1"
                          }
                        ],
                        "functionName": {
                          "name": "abi_decode_t_string_memory_ptr",
                          "nodeType": "YulIdentifier",
                          "src": "1348:30:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1348:63:1"
                      },
                      "variableNames": [
                        {
                          "name": "value1",
                          "nodeType": "YulIdentifier",
                          "src": "1338:6:1"
                        }
                      ]
                    }
                  ]
                }
              ]
            },
            "name": "abi_decode_tuple_t_string_memory_ptrt_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "860:9:1",
                "type": ""
              },
              {
                "name": "dataEnd",
                "nodeType": "YulTypedName",
                "src": "871:7:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "883:6:1",
                "type": ""
              },
              {
                "name": "value1",
                "nodeType": "YulTypedName",
                "src": "891:6:1",
                "type": ""
              }
            ],
            "src": "795:633:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1500:196:1",
              "statements": [
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "1546:16:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "1555:1:1",
                              "type": "",
                              "value": "0"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "1558:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "revert",
                            "nodeType": "YulIdentifier",
                            "src": "1548:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "1548:12:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "1548:12:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "dataEnd",
                            "nodeType": "YulIdentifier",
                            "src": "1521:7:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "1530:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "1517:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1517:23:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "1542:2:1",
                        "type": "",
                        "value": "32"
                      }
                    ],
                    "functionName": {
                      "name": "slt",
                      "nodeType": "YulIdentifier",
                      "src": "1513:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1513:32:1"
                  },
                  "nodeType": "YulIf",
                  "src": "1510:2:1"
                },
                {
                  "nodeType": "YulBlock",
                  "src": "1572:117:1",
                  "statements": [
                    {
                      "nodeType": "YulVariableDeclaration",
                      "src": "1587:15:1",
                      "value": {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "1601:1:1",
                        "type": "",
                        "value": "0"
                      },
                      "variables": [
                        {
                          "name": "offset",
                          "nodeType": "YulTypedName",
                          "src": "1591:6:1",
                          "type": ""
                        }
                      ]
                    },
                    {
                      "nodeType": "YulAssignment",
                      "src": "1616:63:1",
                      "value": {
                        "arguments": [
                          {
                            "arguments": [
                              {
                                "name": "headStart",
                                "nodeType": "YulIdentifier",
                                "src": "1651:9:1"
                              },
                              {
                                "name": "offset",
                                "nodeType": "YulIdentifier",
                                "src": "1662:6:1"
                              }
                            ],
                            "functionName": {
                              "name": "add",
                              "nodeType": "YulIdentifier",
                              "src": "1647:3:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "1647:22:1"
                          },
                          {
                            "name": "dataEnd",
                            "nodeType": "YulIdentifier",
                            "src": "1671:7:1"
                          }
                        ],
                        "functionName": {
                          "name": "abi_decode_t_uint256",
                          "nodeType": "YulIdentifier",
                          "src": "1626:20:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1626:53:1"
                      },
                      "variableNames": [
                        {
                          "name": "value0",
                          "nodeType": "YulIdentifier",
                          "src": "1616:6:1"
                        }
                      ]
                    }
                  ]
                }
              ]
            },
            "name": "abi_decode_tuple_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "1470:9:1",
                "type": ""
              },
              {
                "name": "dataEnd",
                "nodeType": "YulTypedName",
                "src": "1481:7:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "1493:6:1",
                "type": ""
              }
            ],
            "src": "1434:262:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1761:50:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "1778:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "1798:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "cleanup_t_bool",
                          "nodeType": "YulIdentifier",
                          "src": "1783:14:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "1783:21:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "1771:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1771:34:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "1771:34:1"
                }
              ]
            },
            "name": "abi_encode_t_bool_to_t_bool_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "1749:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "1756:3:1",
                "type": ""
              }
            ],
            "src": "1702:109:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "1909:272:1",
              "statements": [
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "1919:53:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "1966:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "array_length_t_string_memory_ptr",
                      "nodeType": "YulIdentifier",
                      "src": "1933:32:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1933:39:1"
                  },
                  "variables": [
                    {
                      "name": "length",
                      "nodeType": "YulTypedName",
                      "src": "1923:6:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "1981:78:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "2047:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "2052:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "array_storeLengthForEncoding_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "1988:58:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "1988:71:1"
                  },
                  "variableNames": [
                    {
                      "name": "pos",
                      "nodeType": "YulIdentifier",
                      "src": "1981:3:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "2094:5:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "2101:4:1",
                            "type": "",
                            "value": "0x20"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "2090:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2090:16:1"
                      },
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "2108:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "2113:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "copy_memory_to_memory",
                      "nodeType": "YulIdentifier",
                      "src": "2068:21:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2068:52:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2068:52:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "2129:46:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "2140:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "2167:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "round_up_to_mul_of_32",
                          "nodeType": "YulIdentifier",
                          "src": "2145:21:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2145:29:1"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "2136:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2136:39:1"
                  },
                  "variableNames": [
                    {
                      "name": "end",
                      "nodeType": "YulIdentifier",
                      "src": "2129:3:1"
                    }
                  ]
                }
              ]
            },
            "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "1890:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "1897:3:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "end",
                "nodeType": "YulTypedName",
                "src": "1905:3:1",
                "type": ""
              }
            ],
            "src": "1817:364:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2252:53:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "2269:3:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "2292:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "cleanup_t_uint256",
                          "nodeType": "YulIdentifier",
                          "src": "2274:17:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2274:24:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "2262:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2262:37:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2262:37:1"
                }
              ]
            },
            "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "2240:5:1",
                "type": ""
              },
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "2247:3:1",
                "type": ""
              }
            ],
            "src": "2187:118:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2409:124:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "2419:26:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "headStart",
                        "nodeType": "YulIdentifier",
                        "src": "2431:9:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2442:2:1",
                        "type": "",
                        "value": "32"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "2427:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2427:18:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "2419:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value0",
                        "nodeType": "YulIdentifier",
                        "src": "2499:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "2512:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "2523:1:1",
                            "type": "",
                            "value": "0"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "2508:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2508:17:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "2455:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2455:71:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2455:71:1"
                }
              ]
            },
            "name": "abi_encode_tuple_t_uint256__to_t_uint256__fromStack_reversed",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "2381:9:1",
                "type": ""
              },
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "2393:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "tail",
                "nodeType": "YulTypedName",
                "src": "2404:4:1",
                "type": ""
              }
            ],
            "src": "2311:222:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "2659:200:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "2669:26:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "headStart",
                        "nodeType": "YulIdentifier",
                        "src": "2681:9:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "2692:2:1",
                        "type": "",
                        "value": "64"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "2677:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2677:18:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "2669:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value0",
                        "nodeType": "YulIdentifier",
                        "src": "2749:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "2762:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "2773:1:1",
                            "type": "",
                            "value": "0"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "2758:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2758:17:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "2705:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2705:71:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2705:71:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value1",
                        "nodeType": "YulIdentifier",
                        "src": "2824:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "2837:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "2848:2:1",
                            "type": "",
                            "value": "32"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "2833:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "2833:18:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_bool_to_t_bool_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "2786:37:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "2786:66:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "2786:66:1"
                }
              ]
            },
            "name": "abi_encode_tuple_t_uint256_t_bool__to_t_uint256_t_bool__fromStack_reversed",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "2623:9:1",
                "type": ""
              },
              {
                "name": "value1",
                "nodeType": "YulTypedName",
                "src": "2635:6:1",
                "type": ""
              },
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "2643:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "tail",
                "nodeType": "YulTypedName",
                "src": "2654:4:1",
                "type": ""
              }
            ],
            "src": "2539:320:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "3109:590:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "3119:27:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "headStart",
                        "nodeType": "YulIdentifier",
                        "src": "3131:9:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3142:3:1",
                        "type": "",
                        "value": "160"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "3127:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3127:19:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "3119:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value0",
                        "nodeType": "YulIdentifier",
                        "src": "3200:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3213:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3224:1:1",
                            "type": "",
                            "value": "0"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3209:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3209:17:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "3156:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3156:71:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3156:71:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3248:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3259:2:1",
                            "type": "",
                            "value": "32"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3244:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3244:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "tail",
                            "nodeType": "YulIdentifier",
                            "src": "3268:4:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3274:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "3264:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3264:20:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "3237:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3237:48:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3237:48:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "3294:86:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value1",
                        "nodeType": "YulIdentifier",
                        "src": "3366:6:1"
                      },
                      {
                        "name": "tail",
                        "nodeType": "YulIdentifier",
                        "src": "3375:4:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "3302:63:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3302:78:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "3294:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3401:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3412:2:1",
                            "type": "",
                            "value": "64"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3397:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3397:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "tail",
                            "nodeType": "YulIdentifier",
                            "src": "3421:4:1"
                          },
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3427:9:1"
                          }
                        ],
                        "functionName": {
                          "name": "sub",
                          "nodeType": "YulIdentifier",
                          "src": "3417:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3417:20:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "3390:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3390:48:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3390:48:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "3447:86:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value2",
                        "nodeType": "YulIdentifier",
                        "src": "3519:6:1"
                      },
                      {
                        "name": "tail",
                        "nodeType": "YulIdentifier",
                        "src": "3528:4:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "3455:63:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3455:78:1"
                  },
                  "variableNames": [
                    {
                      "name": "tail",
                      "nodeType": "YulIdentifier",
                      "src": "3447:4:1"
                    }
                  ]
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value3",
                        "nodeType": "YulIdentifier",
                        "src": "3581:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3594:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3605:2:1",
                            "type": "",
                            "value": "96"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3590:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3590:18:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_bool_to_t_bool_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "3543:37:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3543:66:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3543:66:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "value4",
                        "nodeType": "YulIdentifier",
                        "src": "3663:6:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "headStart",
                            "nodeType": "YulIdentifier",
                            "src": "3676:9:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3687:3:1",
                            "type": "",
                            "value": "128"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "3672:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3672:19:1"
                      }
                    ],
                    "functionName": {
                      "name": "abi_encode_t_uint256_to_t_uint256_fromStack",
                      "nodeType": "YulIdentifier",
                      "src": "3619:43:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3619:73:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3619:73:1"
                }
              ]
            },
            "name": "abi_encode_tuple_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__to_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__fromStack_reversed",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "headStart",
                "nodeType": "YulTypedName",
                "src": "3049:9:1",
                "type": ""
              },
              {
                "name": "value4",
                "nodeType": "YulTypedName",
                "src": "3061:6:1",
                "type": ""
              },
              {
                "name": "value3",
                "nodeType": "YulTypedName",
                "src": "3069:6:1",
                "type": ""
              },
              {
                "name": "value2",
                "nodeType": "YulTypedName",
                "src": "3077:6:1",
                "type": ""
              },
              {
                "name": "value1",
                "nodeType": "YulTypedName",
                "src": "3085:6:1",
                "type": ""
              },
              {
                "name": "value0",
                "nodeType": "YulTypedName",
                "src": "3093:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "tail",
                "nodeType": "YulTypedName",
                "src": "3104:4:1",
                "type": ""
              }
            ],
            "src": "2865:834:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "3745:243:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "3755:19:1",
                  "value": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3771:2:1",
                        "type": "",
                        "value": "64"
                      }
                    ],
                    "functionName": {
                      "name": "mload",
                      "nodeType": "YulIdentifier",
                      "src": "3765:5:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3765:9:1"
                  },
                  "variableNames": [
                    {
                      "name": "memPtr",
                      "nodeType": "YulIdentifier",
                      "src": "3755:6:1"
                    }
                  ]
                },
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "3783:35:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "memPtr",
                        "nodeType": "YulIdentifier",
                        "src": "3805:6:1"
                      },
                      {
                        "name": "size",
                        "nodeType": "YulIdentifier",
                        "src": "3813:4:1"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "3801:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3801:17:1"
                  },
                  "variables": [
                    {
                      "name": "newFreePtr",
                      "nodeType": "YulTypedName",
                      "src": "3787:10:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "3929:22:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x41",
                            "nodeType": "YulIdentifier",
                            "src": "3931:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "3931:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "3931:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "newFreePtr",
                            "nodeType": "YulIdentifier",
                            "src": "3872:10:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "3884:18:1",
                            "type": "",
                            "value": "0xffffffffffffffff"
                          }
                        ],
                        "functionName": {
                          "name": "gt",
                          "nodeType": "YulIdentifier",
                          "src": "3869:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3869:34:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "newFreePtr",
                            "nodeType": "YulIdentifier",
                            "src": "3908:10:1"
                          },
                          {
                            "name": "memPtr",
                            "nodeType": "YulIdentifier",
                            "src": "3920:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "lt",
                          "nodeType": "YulIdentifier",
                          "src": "3905:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "3905:22:1"
                      }
                    ],
                    "functionName": {
                      "name": "or",
                      "nodeType": "YulIdentifier",
                      "src": "3866:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3866:62:1"
                  },
                  "nodeType": "YulIf",
                  "src": "3863:2:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "3967:2:1",
                        "type": "",
                        "value": "64"
                      },
                      {
                        "name": "newFreePtr",
                        "nodeType": "YulIdentifier",
                        "src": "3971:10:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "3960:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "3960:22:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "3960:22:1"
                }
              ]
            },
            "name": "allocateMemory",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "size",
                "nodeType": "YulTypedName",
                "src": "3729:4:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "memPtr",
                "nodeType": "YulTypedName",
                "src": "3738:6:1",
                "type": ""
              }
            ],
            "src": "3705:283:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4061:265:1",
              "statements": [
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "4166:22:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x41",
                            "nodeType": "YulIdentifier",
                            "src": "4168:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "4168:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "4168:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "4138:6:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "4146:18:1",
                        "type": "",
                        "value": "0xffffffffffffffff"
                      }
                    ],
                    "functionName": {
                      "name": "gt",
                      "nodeType": "YulIdentifier",
                      "src": "4135:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4135:30:1"
                  },
                  "nodeType": "YulIf",
                  "src": "4132:2:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "4218:41:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "4234:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "4242:4:1",
                            "type": "",
                            "value": "0x1f"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "4230:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "4230:17:1"
                      },
                      {
                        "arguments": [
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "4253:4:1",
                            "type": "",
                            "value": "0x1f"
                          }
                        ],
                        "functionName": {
                          "name": "not",
                          "nodeType": "YulIdentifier",
                          "src": "4249:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "4249:9:1"
                      }
                    ],
                    "functionName": {
                      "name": "and",
                      "nodeType": "YulIdentifier",
                      "src": "4226:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4226:33:1"
                  },
                  "variableNames": [
                    {
                      "name": "size",
                      "nodeType": "YulIdentifier",
                      "src": "4218:4:1"
                    }
                  ]
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "4296:23:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "size",
                        "nodeType": "YulIdentifier",
                        "src": "4308:4:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "4314:4:1",
                        "type": "",
                        "value": "0x20"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "4304:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4304:15:1"
                  },
                  "variableNames": [
                    {
                      "name": "size",
                      "nodeType": "YulIdentifier",
                      "src": "4296:4:1"
                    }
                  ]
                }
              ]
            },
            "name": "array_allocation_size_t_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "4045:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "size",
                "nodeType": "YulTypedName",
                "src": "4056:4:1",
                "type": ""
              }
            ],
            "src": "3994:332:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4391:40:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "4402:22:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "4418:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "mload",
                      "nodeType": "YulIdentifier",
                      "src": "4412:5:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4412:12:1"
                  },
                  "variableNames": [
                    {
                      "name": "length",
                      "nodeType": "YulIdentifier",
                      "src": "4402:6:1"
                    }
                  ]
                }
              ]
            },
            "name": "array_length_t_string_memory_ptr",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "4374:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "4384:6:1",
                "type": ""
              }
            ],
            "src": "4332:99:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4533:73:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "4550:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "4555:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "4543:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4543:19:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "4543:19:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "4571:29:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "pos",
                        "nodeType": "YulIdentifier",
                        "src": "4590:3:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "4595:4:1",
                        "type": "",
                        "value": "0x20"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "4586:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4586:14:1"
                  },
                  "variableNames": [
                    {
                      "name": "updated_pos",
                      "nodeType": "YulIdentifier",
                      "src": "4571:11:1"
                    }
                  ]
                }
              ]
            },
            "name": "array_storeLengthForEncoding_t_string_memory_ptr_fromStack",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "pos",
                "nodeType": "YulTypedName",
                "src": "4505:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "4510:6:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "updated_pos",
                "nodeType": "YulTypedName",
                "src": "4521:11:1",
                "type": ""
              }
            ],
            "src": "4437:169:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4654:48:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "4664:32:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "4689:5:1"
                          }
                        ],
                        "functionName": {
                          "name": "iszero",
                          "nodeType": "YulIdentifier",
                          "src": "4682:6:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "4682:13:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "4675:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4675:21:1"
                  },
                  "variableNames": [
                    {
                      "name": "cleaned",
                      "nodeType": "YulIdentifier",
                      "src": "4664:7:1"
                    }
                  ]
                }
              ]
            },
            "name": "cleanup_t_bool",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "4636:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "cleaned",
                "nodeType": "YulTypedName",
                "src": "4646:7:1",
                "type": ""
              }
            ],
            "src": "4612:90:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4753:32:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "4763:16:1",
                  "value": {
                    "name": "value",
                    "nodeType": "YulIdentifier",
                    "src": "4774:5:1"
                  },
                  "variableNames": [
                    {
                      "name": "cleaned",
                      "nodeType": "YulIdentifier",
                      "src": "4763:7:1"
                    }
                  ]
                }
              ]
            },
            "name": "cleanup_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "4735:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "cleaned",
                "nodeType": "YulTypedName",
                "src": "4745:7:1",
                "type": ""
              }
            ],
            "src": "4708:77:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "4842:103:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "name": "dst",
                        "nodeType": "YulIdentifier",
                        "src": "4865:3:1"
                      },
                      {
                        "name": "src",
                        "nodeType": "YulIdentifier",
                        "src": "4870:3:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "4875:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "calldatacopy",
                      "nodeType": "YulIdentifier",
                      "src": "4852:12:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4852:30:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "4852:30:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "dst",
                            "nodeType": "YulIdentifier",
                            "src": "4923:3:1"
                          },
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "4928:6:1"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "4919:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "4919:16:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "4937:1:1",
                        "type": "",
                        "value": "0"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "4912:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "4912:27:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "4912:27:1"
                }
              ]
            },
            "name": "copy_calldata_to_memory",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "src",
                "nodeType": "YulTypedName",
                "src": "4824:3:1",
                "type": ""
              },
              {
                "name": "dst",
                "nodeType": "YulTypedName",
                "src": "4829:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "4834:6:1",
                "type": ""
              }
            ],
            "src": "4791:154:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "5000:258:1",
              "statements": [
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "5010:10:1",
                  "value": {
                    "kind": "number",
                    "nodeType": "YulLiteral",
                    "src": "5019:1:1",
                    "type": "",
                    "value": "0"
                  },
                  "variables": [
                    {
                      "name": "i",
                      "nodeType": "YulTypedName",
                      "src": "5014:1:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "5079:63:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "arguments": [
                                {
                                  "name": "dst",
                                  "nodeType": "YulIdentifier",
                                  "src": "5104:3:1"
                                },
                                {
                                  "name": "i",
                                  "nodeType": "YulIdentifier",
                                  "src": "5109:1:1"
                                }
                              ],
                              "functionName": {
                                "name": "add",
                                "nodeType": "YulIdentifier",
                                "src": "5100:3:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "5100:11:1"
                            },
                            {
                              "arguments": [
                                {
                                  "arguments": [
                                    {
                                      "name": "src",
                                      "nodeType": "YulIdentifier",
                                      "src": "5123:3:1"
                                    },
                                    {
                                      "name": "i",
                                      "nodeType": "YulIdentifier",
                                      "src": "5128:1:1"
                                    }
                                  ],
                                  "functionName": {
                                    "name": "add",
                                    "nodeType": "YulIdentifier",
                                    "src": "5119:3:1"
                                  },
                                  "nodeType": "YulFunctionCall",
                                  "src": "5119:11:1"
                                }
                              ],
                              "functionName": {
                                "name": "mload",
                                "nodeType": "YulIdentifier",
                                "src": "5113:5:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "5113:18:1"
                            }
                          ],
                          "functionName": {
                            "name": "mstore",
                            "nodeType": "YulIdentifier",
                            "src": "5093:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5093:39:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "5093:39:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "i",
                        "nodeType": "YulIdentifier",
                        "src": "5040:1:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "5043:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "lt",
                      "nodeType": "YulIdentifier",
                      "src": "5037:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5037:13:1"
                  },
                  "nodeType": "YulForLoop",
                  "post": {
                    "nodeType": "YulBlock",
                    "src": "5051:19:1",
                    "statements": [
                      {
                        "nodeType": "YulAssignment",
                        "src": "5053:15:1",
                        "value": {
                          "arguments": [
                            {
                              "name": "i",
                              "nodeType": "YulIdentifier",
                              "src": "5062:1:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "5065:2:1",
                              "type": "",
                              "value": "32"
                            }
                          ],
                          "functionName": {
                            "name": "add",
                            "nodeType": "YulIdentifier",
                            "src": "5058:3:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5058:10:1"
                        },
                        "variableNames": [
                          {
                            "name": "i",
                            "nodeType": "YulIdentifier",
                            "src": "5053:1:1"
                          }
                        ]
                      }
                    ]
                  },
                  "pre": {
                    "nodeType": "YulBlock",
                    "src": "5033:3:1",
                    "statements": []
                  },
                  "src": "5029:113:1"
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "5176:76:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "arguments": [
                                {
                                  "name": "dst",
                                  "nodeType": "YulIdentifier",
                                  "src": "5226:3:1"
                                },
                                {
                                  "name": "length",
                                  "nodeType": "YulIdentifier",
                                  "src": "5231:6:1"
                                }
                              ],
                              "functionName": {
                                "name": "add",
                                "nodeType": "YulIdentifier",
                                "src": "5222:3:1"
                              },
                              "nodeType": "YulFunctionCall",
                              "src": "5222:16:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "5240:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "mstore",
                            "nodeType": "YulIdentifier",
                            "src": "5215:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5215:27:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "5215:27:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "i",
                        "nodeType": "YulIdentifier",
                        "src": "5157:1:1"
                      },
                      {
                        "name": "length",
                        "nodeType": "YulIdentifier",
                        "src": "5160:6:1"
                      }
                    ],
                    "functionName": {
                      "name": "gt",
                      "nodeType": "YulIdentifier",
                      "src": "5154:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5154:13:1"
                  },
                  "nodeType": "YulIf",
                  "src": "5151:2:1"
                }
              ]
            },
            "name": "copy_memory_to_memory",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "src",
                "nodeType": "YulTypedName",
                "src": "4982:3:1",
                "type": ""
              },
              {
                "name": "dst",
                "nodeType": "YulTypedName",
                "src": "4987:3:1",
                "type": ""
              },
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "4992:6:1",
                "type": ""
              }
            ],
            "src": "4951:307:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "5315:269:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "5325:22:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "data",
                        "nodeType": "YulIdentifier",
                        "src": "5339:4:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5345:1:1",
                        "type": "",
                        "value": "2"
                      }
                    ],
                    "functionName": {
                      "name": "div",
                      "nodeType": "YulIdentifier",
                      "src": "5335:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5335:12:1"
                  },
                  "variableNames": [
                    {
                      "name": "length",
                      "nodeType": "YulIdentifier",
                      "src": "5325:6:1"
                    }
                  ]
                },
                {
                  "nodeType": "YulVariableDeclaration",
                  "src": "5356:38:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "data",
                        "nodeType": "YulIdentifier",
                        "src": "5386:4:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5392:1:1",
                        "type": "",
                        "value": "1"
                      }
                    ],
                    "functionName": {
                      "name": "and",
                      "nodeType": "YulIdentifier",
                      "src": "5382:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5382:12:1"
                  },
                  "variables": [
                    {
                      "name": "outOfPlaceEncoding",
                      "nodeType": "YulTypedName",
                      "src": "5360:18:1",
                      "type": ""
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "5433:51:1",
                    "statements": [
                      {
                        "nodeType": "YulAssignment",
                        "src": "5447:27:1",
                        "value": {
                          "arguments": [
                            {
                              "name": "length",
                              "nodeType": "YulIdentifier",
                              "src": "5461:6:1"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "5469:4:1",
                              "type": "",
                              "value": "0x7f"
                            }
                          ],
                          "functionName": {
                            "name": "and",
                            "nodeType": "YulIdentifier",
                            "src": "5457:3:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5457:17:1"
                        },
                        "variableNames": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "5447:6:1"
                          }
                        ]
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "outOfPlaceEncoding",
                        "nodeType": "YulIdentifier",
                        "src": "5413:18:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "5406:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5406:26:1"
                  },
                  "nodeType": "YulIf",
                  "src": "5403:2:1"
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "5536:42:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x22",
                            "nodeType": "YulIdentifier",
                            "src": "5550:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5550:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "5550:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "outOfPlaceEncoding",
                        "nodeType": "YulIdentifier",
                        "src": "5500:18:1"
                      },
                      {
                        "arguments": [
                          {
                            "name": "length",
                            "nodeType": "YulIdentifier",
                            "src": "5523:6:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "5531:2:1",
                            "type": "",
                            "value": "32"
                          }
                        ],
                        "functionName": {
                          "name": "lt",
                          "nodeType": "YulIdentifier",
                          "src": "5520:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "5520:14:1"
                      }
                    ],
                    "functionName": {
                      "name": "eq",
                      "nodeType": "YulIdentifier",
                      "src": "5497:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5497:38:1"
                  },
                  "nodeType": "YulIf",
                  "src": "5494:2:1"
                }
              ]
            },
            "name": "extract_byte_array_length",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "data",
                "nodeType": "YulTypedName",
                "src": "5299:4:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "length",
                "nodeType": "YulTypedName",
                "src": "5308:6:1",
                "type": ""
              }
            ],
            "src": "5264:320:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "5633:190:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "5643:33:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "5670:5:1"
                      }
                    ],
                    "functionName": {
                      "name": "cleanup_t_uint256",
                      "nodeType": "YulIdentifier",
                      "src": "5652:17:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5652:24:1"
                  },
                  "variableNames": [
                    {
                      "name": "value",
                      "nodeType": "YulIdentifier",
                      "src": "5643:5:1"
                    }
                  ]
                },
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "5766:22:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [],
                          "functionName": {
                            "name": "panic_error_0x11",
                            "nodeType": "YulIdentifier",
                            "src": "5768:16:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "5768:18:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "5768:18:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "5691:5:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5698:66:1",
                        "type": "",
                        "value": "0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff"
                      }
                    ],
                    "functionName": {
                      "name": "eq",
                      "nodeType": "YulIdentifier",
                      "src": "5688:2:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5688:77:1"
                  },
                  "nodeType": "YulIf",
                  "src": "5685:2:1"
                },
                {
                  "nodeType": "YulAssignment",
                  "src": "5797:20:1",
                  "value": {
                    "arguments": [
                      {
                        "name": "value",
                        "nodeType": "YulIdentifier",
                        "src": "5808:5:1"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5815:1:1",
                        "type": "",
                        "value": "1"
                      }
                    ],
                    "functionName": {
                      "name": "add",
                      "nodeType": "YulIdentifier",
                      "src": "5804:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5804:13:1"
                  },
                  "variableNames": [
                    {
                      "name": "ret",
                      "nodeType": "YulIdentifier",
                      "src": "5797:3:1"
                    }
                  ]
                }
              ]
            },
            "name": "increment_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "5619:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "ret",
                "nodeType": "YulTypedName",
                "src": "5629:3:1",
                "type": ""
              }
            ],
            "src": "5590:233:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "5857:152:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5874:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5877:77:1",
                        "type": "",
                        "value": "35408467139433450592217433187231851964531694900788300625387963629091585785856"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "5867:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5867:88:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "5867:88:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5971:1:1",
                        "type": "",
                        "value": "4"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5974:4:1",
                        "type": "",
                        "value": "0x11"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "5964:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5964:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "5964:15:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5995:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "5998:4:1",
                        "type": "",
                        "value": "0x24"
                      }
                    ],
                    "functionName": {
                      "name": "revert",
                      "nodeType": "YulIdentifier",
                      "src": "5988:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "5988:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "5988:15:1"
                }
              ]
            },
            "name": "panic_error_0x11",
            "nodeType": "YulFunctionDefinition",
            "src": "5829:180:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "6043:152:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6060:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6063:77:1",
                        "type": "",
                        "value": "35408467139433450592217433187231851964531694900788300625387963629091585785856"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "6053:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6053:88:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6053:88:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6157:1:1",
                        "type": "",
                        "value": "4"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6160:4:1",
                        "type": "",
                        "value": "0x22"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "6150:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6150:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6150:15:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6181:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6184:4:1",
                        "type": "",
                        "value": "0x24"
                      }
                    ],
                    "functionName": {
                      "name": "revert",
                      "nodeType": "YulIdentifier",
                      "src": "6174:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6174:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6174:15:1"
                }
              ]
            },
            "name": "panic_error_0x22",
            "nodeType": "YulFunctionDefinition",
            "src": "6015:180:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "6229:152:1",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6246:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6249:77:1",
                        "type": "",
                        "value": "35408467139433450592217433187231851964531694900788300625387963629091585785856"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "6239:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6239:88:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6239:88:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6343:1:1",
                        "type": "",
                        "value": "4"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6346:4:1",
                        "type": "",
                        "value": "0x41"
                      }
                    ],
                    "functionName": {
                      "name": "mstore",
                      "nodeType": "YulIdentifier",
                      "src": "6336:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6336:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6336:15:1"
                },
                {
                  "expression": {
                    "arguments": [
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6367:1:1",
                        "type": "",
                        "value": "0"
                      },
                      {
                        "kind": "number",
                        "nodeType": "YulLiteral",
                        "src": "6370:4:1",
                        "type": "",
                        "value": "0x24"
                      }
                    ],
                    "functionName": {
                      "name": "revert",
                      "nodeType": "YulIdentifier",
                      "src": "6360:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6360:15:1"
                  },
                  "nodeType": "YulExpressionStatement",
                  "src": "6360:15:1"
                }
              ]
            },
            "name": "panic_error_0x41",
            "nodeType": "YulFunctionDefinition",
            "src": "6201:180:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "6435:54:1",
              "statements": [
                {
                  "nodeType": "YulAssignment",
                  "src": "6445:38:1",
                  "value": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "6463:5:1"
                          },
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "6470:2:1",
                            "type": "",
                            "value": "31"
                          }
                        ],
                        "functionName": {
                          "name": "add",
                          "nodeType": "YulIdentifier",
                          "src": "6459:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "6459:14:1"
                      },
                      {
                        "arguments": [
                          {
                            "kind": "number",
                            "nodeType": "YulLiteral",
                            "src": "6479:2:1",
                            "type": "",
                            "value": "31"
                          }
                        ],
                        "functionName": {
                          "name": "not",
                          "nodeType": "YulIdentifier",
                          "src": "6475:3:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "6475:7:1"
                      }
                    ],
                    "functionName": {
                      "name": "and",
                      "nodeType": "YulIdentifier",
                      "src": "6455:3:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6455:28:1"
                  },
                  "variableNames": [
                    {
                      "name": "result",
                      "nodeType": "YulIdentifier",
                      "src": "6445:6:1"
                    }
                  ]
                }
              ]
            },
            "name": "round_up_to_mul_of_32",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "6418:5:1",
                "type": ""
              }
            ],
            "returnVariables": [
              {
                "name": "result",
                "nodeType": "YulTypedName",
                "src": "6428:6:1",
                "type": ""
              }
            ],
            "src": "6387:102:1"
          },
          {
            "body": {
              "nodeType": "YulBlock",
              "src": "6538:79:1",
              "statements": [
                {
                  "body": {
                    "nodeType": "YulBlock",
                    "src": "6595:16:1",
                    "statements": [
                      {
                        "expression": {
                          "arguments": [
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "6604:1:1",
                              "type": "",
                              "value": "0"
                            },
                            {
                              "kind": "number",
                              "nodeType": "YulLiteral",
                              "src": "6607:1:1",
                              "type": "",
                              "value": "0"
                            }
                          ],
                          "functionName": {
                            "name": "revert",
                            "nodeType": "YulIdentifier",
                            "src": "6597:6:1"
                          },
                          "nodeType": "YulFunctionCall",
                          "src": "6597:12:1"
                        },
                        "nodeType": "YulExpressionStatement",
                        "src": "6597:12:1"
                      }
                    ]
                  },
                  "condition": {
                    "arguments": [
                      {
                        "arguments": [
                          {
                            "name": "value",
                            "nodeType": "YulIdentifier",
                            "src": "6561:5:1"
                          },
                          {
                            "arguments": [
                              {
                                "name": "value",
                                "nodeType": "YulIdentifier",
                                "src": "6586:5:1"
                              }
                            ],
                            "functionName": {
                              "name": "cleanup_t_uint256",
                              "nodeType": "YulIdentifier",
                              "src": "6568:17:1"
                            },
                            "nodeType": "YulFunctionCall",
                            "src": "6568:24:1"
                          }
                        ],
                        "functionName": {
                          "name": "eq",
                          "nodeType": "YulIdentifier",
                          "src": "6558:2:1"
                        },
                        "nodeType": "YulFunctionCall",
                        "src": "6558:35:1"
                      }
                    ],
                    "functionName": {
                      "name": "iszero",
                      "nodeType": "YulIdentifier",
                      "src": "6551:6:1"
                    },
                    "nodeType": "YulFunctionCall",
                    "src": "6551:43:1"
                  },
                  "nodeType": "YulIf",
                  "src": "6548:2:1"
                }
              ]
            },
            "name": "validator_revert_t_uint256",
            "nodeType": "YulFunctionDefinition",
            "parameters": [
              {
                "name": "value",
                "nodeType": "YulTypedName",
                "src": "6531:5:1",
                "type": ""
              }
            ],
            "src": "6495:122:1"
          }
        ]
      },
      "contents": "{\n\n    function abi_decode_available_length_t_string_memory_ptr(src, length, end) -> array {\n        array := allocateMemory(array_allocation_size_t_string_memory_ptr(length))\n        mstore(array, length)\n        let dst := add(array, 0x20)\n        if gt(add(src, length), end) { revert(0, 0) }\n        copy_calldata_to_memory(src, dst, length)\n    }\n\n    // string\n    function abi_decode_t_string_memory_ptr(offset, end) -> array {\n        if iszero(slt(add(offset, 0x1f), end)) { revert(0, 0) }\n        let length := calldataload(offset)\n        array := abi_decode_available_length_t_string_memory_ptr(add(offset, 0x20), length, end)\n    }\n\n    function abi_decode_t_uint256(offset, end) -> value {\n        value := calldataload(offset)\n        validator_revert_t_uint256(value)\n    }\n\n    function abi_decode_tuple_t_string_memory_ptrt_string_memory_ptr(headStart, dataEnd) -> value0, value1 {\n        if slt(sub(dataEnd, headStart), 64) { revert(0, 0) }\n\n        {\n\n            let offset := calldataload(add(headStart, 0))\n            if gt(offset, 0xffffffffffffffff) { revert(0, 0) }\n\n            value0 := abi_decode_t_string_memory_ptr(add(headStart, offset), dataEnd)\n        }\n\n        {\n\n            let offset := calldataload(add(headStart, 32))\n            if gt(offset, 0xffffffffffffffff) { revert(0, 0) }\n\n            value1 := abi_decode_t_string_memory_ptr(add(headStart, offset), dataEnd)\n        }\n\n    }\n\n    function abi_decode_tuple_t_uint256(headStart, dataEnd) -> value0 {\n        if slt(sub(dataEnd, headStart), 32) { revert(0, 0) }\n\n        {\n\n            let offset := 0\n\n            value0 := abi_decode_t_uint256(add(headStart, offset), dataEnd)\n        }\n\n    }\n\n    function abi_encode_t_bool_to_t_bool_fromStack(value, pos) {\n        mstore(pos, cleanup_t_bool(value))\n    }\n\n    function abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value, pos) -> end {\n        let length := array_length_t_string_memory_ptr(value)\n        pos := array_storeLengthForEncoding_t_string_memory_ptr_fromStack(pos, length)\n        copy_memory_to_memory(add(value, 0x20), pos, length)\n        end := add(pos, round_up_to_mul_of_32(length))\n    }\n\n    function abi_encode_t_uint256_to_t_uint256_fromStack(value, pos) {\n        mstore(pos, cleanup_t_uint256(value))\n    }\n\n    function abi_encode_tuple_t_uint256__to_t_uint256__fromStack_reversed(headStart , value0) -> tail {\n        tail := add(headStart, 32)\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value0,  add(headStart, 0))\n\n    }\n\n    function abi_encode_tuple_t_uint256_t_bool__to_t_uint256_t_bool__fromStack_reversed(headStart , value1, value0) -> tail {\n        tail := add(headStart, 64)\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value0,  add(headStart, 0))\n\n        abi_encode_t_bool_to_t_bool_fromStack(value1,  add(headStart, 32))\n\n    }\n\n    function abi_encode_tuple_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__to_t_uint256_t_string_memory_ptr_t_string_memory_ptr_t_bool_t_uint256__fromStack_reversed(headStart , value4, value3, value2, value1, value0) -> tail {\n        tail := add(headStart, 160)\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value0,  add(headStart, 0))\n\n        mstore(add(headStart, 32), sub(tail, headStart))\n        tail := abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value1,  tail)\n\n        mstore(add(headStart, 64), sub(tail, headStart))\n        tail := abi_encode_t_string_memory_ptr_to_t_string_memory_ptr_fromStack(value2,  tail)\n\n        abi_encode_t_bool_to_t_bool_fromStack(value3,  add(headStart, 96))\n\n        abi_encode_t_uint256_to_t_uint256_fromStack(value4,  add(headStart, 128))\n\n    }\n\n    function allocateMemory(size) -> memPtr {\n        memPtr := mload(64)\n        let newFreePtr := add(memPtr, size)\n        // protect against overflow\n        if or(gt(newFreePtr, 0xffffffffffffffff), lt(newFreePtr, memPtr)) { panic_error_0x41() }\n        mstore(64, newFreePtr)\n    }\n\n    function array_allocation_size_t_string_memory_ptr(length) -> size {\n        // Make sure we can allocate memory without overflow\n        if gt(length, 0xffffffffffffffff) { panic_error_0x41() }\n\n        // round up\n        size := and(add(length, 0x1f), not(0x1f))\n\n        // add length slot\n        size := add(size, 0x20)\n\n    }\n\n    function array_length_t_string_memory_ptr(value) -> length {\n\n        length := mload(value)\n\n    }\n\n    function array_storeLengthForEncoding_t_string_memory_ptr_fromStack(pos, length) -> updated_pos {\n        mstore(pos, length)\n        updated_pos := add(pos, 0x20)\n    }\n\n    function cleanup_t_bool(value) -> cleaned {\n        cleaned := iszero(iszero(value))\n    }\n\n    function cleanup_t_uint256(value) -> cleaned {\n        cleaned := value\n    }\n\n    function copy_calldata_to_memory(src, dst, length) {\n        calldatacopy(dst, src, length)\n        // clear end\n        mstore(add(dst, length), 0)\n    }\n\n    function copy_memory_to_memory(src, dst, length) {\n        let i := 0\n        for { } lt(i, length) { i := add(i, 32) }\n        {\n            mstore(add(dst, i), mload(add(src, i)))\n        }\n        if gt(i, length)\n        {\n            // clear end\n            mstore(add(dst, length), 0)\n        }\n    }\n\n    function extract_byte_array_length(data) -> length {\n        length := div(data, 2)\n        let outOfPlaceEncoding := and(data, 1)\n        if iszero(outOfPlaceEncoding) {\n            length := and(length, 0x7f)\n        }\n\n        if eq(outOfPlaceEncoding, lt(length, 32)) {\n            panic_error_0x22()\n        }\n    }\n\n    function increment_t_uint256(value) -> ret {\n        value := cleanup_t_uint256(value)\n        if eq(value, 0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff) { panic_error_0x11() }\n        ret := add(value, 1)\n    }\n\n    function panic_error_0x11() {\n        mstore(0, 35408467139433450592217433187231851964531694900788300625387963629091585785856)\n        mstore(4, 0x11)\n        revert(0, 0x24)\n    }\n\n    function panic_error_0x22() {\n        mstore(0, 35408467139433450592217433187231851964531694900788300625387963629091585785856)\n        mstore(4, 0x22)\n        revert(0, 0x24)\n    }\n\n    function panic_error_0x41() {\n        mstore(0, 35408467139433450592217433187231851964531694900788300625387963629091585785856)\n        mstore(4, 0x41)\n        revert(0, 0x24)\n    }\n\n    function round_up_to_mul_of_32(value) -> result {\n        result := and(add(value, 31), not(31))\n    }\n\n    function validator_revert_t_uint256(value) {\n        if iszero(eq(value, cleanup_t_uint256(value))) { revert(0, 0) }\n    }\n\n}\n",
      "id": 1,
      "language": "Yul",
      "name": "#utility.yul"
    }
  ],
  "sourceMap": "69:967:0:-:0;;;125:1;99:27;;133:76;;;;;;;;;;155:48;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:10;;;:48;;:::i;:::-;69:967;;566:276;650:11;;:13;;;;;;;;;:::i;:::-;;;;;;691:63;;;;;;;;696:11;;691:63;;;;709:6;691:63;;;;717:12;691:63;;;;731:5;691:63;;;;;;738:15;691:63;;;670:5;:18;676:11;;670:18;;;;;;;;;;;:84;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;766:70;778:11;;791:6;799:12;813:5;820:15;766:70;;;;;;;;;;:::i;:::-;;;;;;;;566:276;;:::o;69:967::-;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;:::o;:::-;;;;;;;;;;;;;;;;;;;;;:::o;7:109:1:-;88:21;103:5;88:21;:::i;:::-;83:3;76:34;66:50;;:::o;122:364::-;;238:39;271:5;238:39;:::i;:::-;293:71;357:6;352:3;293:71;:::i;:::-;286:78;;373:52;418:6;413:3;406:4;399:5;395:16;373:52;:::i;:::-;450:29;472:6;450:29;:::i;:::-;445:3;441:39;434:46;;214:272;;;;;:::o;492:118::-;579:24;597:5;579:24;:::i;:::-;574:3;567:37;557:53;;:::o;616:834::-;;893:3;882:9;878:19;870:27;;907:71;975:1;964:9;960:17;951:6;907:71;:::i;:::-;1025:9;1019:4;1015:20;1010:2;999:9;995:18;988:48;1053:78;1126:4;1117:6;1053:78;:::i;:::-;1045:86;;1178:9;1172:4;1168:20;1163:2;1152:9;1148:18;1141:48;1206:78;1279:4;1270:6;1206:78;:::i;:::-;1198:86;;1294:66;1356:2;1345:9;1341:18;1332:6;1294:66;:::i;:::-;1370:73;1438:3;1427:9;1423:19;1414:6;1370:73;:::i;:::-;860:590;;;;;;;;:::o;1456:99::-;;1542:5;1536:12;1526:22;;1515:40;;;:::o;1561:169::-;;1679:6;1674:3;1667:19;1719:4;1714:3;1710:14;1695:29;;1657:73;;;;:::o;1736:90::-;;1813:5;1806:13;1799:21;1788:32;;1778:48;;;:::o;1832:77::-;;1898:5;1887:16;;1877:32;;;:::o;1915:307::-;1983:1;1993:113;2007:6;2004:1;2001:13;1993:113;;;2092:1;2087:3;2083:11;2077:18;2073:1;2068:3;2064:11;2057:39;2029:2;2026:1;2022:10;2017:15;;1993:113;;;2124:6;2121:1;2118:13;2115:2;;;2204:1;2195:6;2190:3;2186:16;2179:27;2115:2;1964:258;;;;:::o;2228:320::-;;2309:1;2303:4;2299:12;2289:22;;2356:1;2350:4;2346:12;2377:18;2367:2;;2433:4;2425:6;2421:17;2411:27;;2367:2;2495;2487:6;2484:14;2464:18;2461:38;2458:2;;;2514:18;;:::i;:::-;2458:2;2279:269;;;;:::o;2554:233::-;;2616:24;2634:5;2616:24;:::i;:::-;2607:33;;2662:66;2655:5;2652:77;2649:2;;;2732:18;;:::i;:::-;2649:2;2779:1;2772:5;2768:13;2761:20;;2597:190;;;:::o;2793:180::-;2841:77;2838:1;2831:88;2938:4;2935:1;2928:15;2962:4;2959:1;2952:15;2979:180;3027:77;3024:1;3017:88;3124:4;3121:1;3114:15;3148:4;3145:1;3138:15;3165:102;;3257:2;3253:7;3248:2;3241:5;3237:14;3233:28;3223:38;;3213:54;;;:::o;69:967:0:-;;;;;;;",
  "deployedSourceMap": "69:967:0:-:0;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;566:276;;;;;;;;;;;;;:::i;:::-;;:::i;:::-;;99:27;;;:::i;:::-;;;;;;;:::i;:::-;;;;;;;;521:38;;;;;;;;;;;;;:::i;:::-;;:::i;:::-;;;;;;;;;;;:::i;:::-;;;;;;;;848:183;;;;;;;;;;;;;:::i;:::-;;:::i;:::-;;566:276;650:11;;:13;;;;;;;;;:::i;:::-;;;;;;691:63;;;;;;;;696:11;;691:63;;;;709:6;691:63;;;;717:12;691:63;;;;731:5;691:63;;;;;;738:15;691:63;;;670:5;:18;676:11;;670:18;;;;;;;;;;;:84;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;766:70;778:11;;791:6;799:12;813:5;820:15;766:70;;;;;;;;;;:::i;:::-;;;;;;;;566:276;;:::o;99:27::-;;;;:::o;521:38::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::o;848:183::-;895:17;915:5;:10;921:3;915:10;;;;;;;;;;;895:30;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;946:5;:10;;;945:11;932:5;:10;;:24;;;;;;;;;;;976:5;963;:10;969:3;963:10;;;;;;;;;;;:18;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;993:32;1009:3;1014:5;:10;;;993:32;;;;;;;:::i;:::-;;;;;;;;848:183;;:::o;-1:-1:-1:-;;;;;;;:::i;:::-;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:::i;:::-;;;:::o;:::-;;;;;;;;;;;;;;;;;;;;;:::o;7:344:1:-;;110:65;125:49;167:6;125:49;:::i;:::-;110:65;:::i;:::-;101:74;;198:6;191:5;184:21;236:4;229:5;225:16;274:3;265:6;260:3;256:16;253:25;250:2;;;291:1;288;281:12;250:2;304:41;338:6;333:3;328;304:41;:::i;:::-;91:260;;;;;;:::o;371:273::-;;476:3;469:4;461:6;457:17;453:27;443:2;;494:1;491;484:12;443:2;534:6;521:20;559:79;634:3;626:6;619:4;611:6;607:17;559:79;:::i;:::-;550:88;;433:211;;;;;:::o;650:139::-;;734:6;721:20;712:29;;750:33;777:5;750:33;:::i;:::-;702:87;;;;:::o;795:633::-;;;940:2;928:9;919:7;915:23;911:32;908:2;;;956:1;953;946:12;908:2;1027:1;1016:9;1012:17;999:31;1057:18;1049:6;1046:30;1043:2;;;1089:1;1086;1079:12;1043:2;1117:63;1172:7;1163:6;1152:9;1148:22;1117:63;:::i;:::-;1107:73;;970:220;1257:2;1246:9;1242:18;1229:32;1288:18;1280:6;1277:30;1274:2;;;1320:1;1317;1310:12;1274:2;1348:63;1403:7;1394:6;1383:9;1379:22;1348:63;:::i;:::-;1338:73;;1200:221;898:530;;;;;:::o;1434:262::-;;1542:2;1530:9;1521:7;1517:23;1513:32;1510:2;;;1558:1;1555;1548:12;1510:2;1601:1;1626:53;1671:7;1662:6;1651:9;1647:22;1626:53;:::i;:::-;1616:63;;1572:117;1500:196;;;;:::o;1702:109::-;1783:21;1798:5;1783:21;:::i;:::-;1778:3;1771:34;1761:50;;:::o;1817:364::-;;1933:39;1966:5;1933:39;:::i;:::-;1988:71;2052:6;2047:3;1988:71;:::i;:::-;1981:78;;2068:52;2113:6;2108:3;2101:4;2094:5;2090:16;2068:52;:::i;:::-;2145:29;2167:6;2145:29;:::i;:::-;2140:3;2136:39;2129:46;;1909:272;;;;;:::o;2187:118::-;2274:24;2292:5;2274:24;:::i;:::-;2269:3;2262:37;2252:53;;:::o;2311:222::-;;2442:2;2431:9;2427:18;2419:26;;2455:71;2523:1;2512:9;2508:17;2499:6;2455:71;:::i;:::-;2409:124;;;;:::o;2539:320::-;;2692:2;2681:9;2677:18;2669:26;;2705:71;2773:1;2762:9;2758:17;2749:6;2705:71;:::i;:::-;2786:66;2848:2;2837:9;2833:18;2824:6;2786:66;:::i;:::-;2659:200;;;;;:::o;2865:834::-;;3142:3;3131:9;3127:19;3119:27;;3156:71;3224:1;3213:9;3209:17;3200:6;3156:71;:::i;:::-;3274:9;3268:4;3264:20;3259:2;3248:9;3244:18;3237:48;3302:78;3375:4;3366:6;3302:78;:::i;:::-;3294:86;;3427:9;3421:4;3417:20;3412:2;3401:9;3397:18;3390:48;3455:78;3528:4;3519:6;3455:78;:::i;:::-;3447:86;;3543:66;3605:2;3594:9;3590:18;3581:6;3543:66;:::i;:::-;3619:73;3687:3;3676:9;3672:19;3663:6;3619:73;:::i;:::-;3109:590;;;;;;;;:::o;3705:283::-;;3771:2;3765:9;3755:19;;3813:4;3805:6;3801:17;3920:6;3908:10;3905:22;3884:18;3872:10;3869:34;3866:62;3863:2;;;3931:18;;:::i;:::-;3863:2;3971:10;3967:2;3960:22;3745:243;;;;:::o;3994:332::-;;4146:18;4138:6;4135:30;4132:2;;;4168:18;;:::i;:::-;4132:2;4253:4;4249:9;4242:4;4234:6;4230:17;4226:33;4218:41;;4314:4;4308;4304:15;4296:23;;4061:265;;;:::o;4332:99::-;;4418:5;4412:12;4402:22;;4391:40;;;:::o;4437:169::-;;4555:6;4550:3;4543:19;4595:4;4590:3;4586:14;4571:29;;4533:73;;;;:::o;4612:90::-;;4689:5;4682:13;4675:21;4664:32;;4654:48;;;:::o;4708:77::-;;4774:5;4763:16;;4753:32;;;:::o;4791:154::-;4875:6;4870:3;4865;4852:30;4937:1;4928:6;4923:3;4919:16;4912:27;4842:103;;;:::o;4951:307::-;5019:1;5029:113;5043:6;5040:1;5037:13;5029:113;;;5128:1;5123:3;5119:11;5113:18;5109:1;5104:3;5100:11;5093:39;5065:2;5062:1;5058:10;5053:15;;5029:113;;;5160:6;5157:1;5154:13;5151:2;;;5240:1;5231:6;5226:3;5222:16;5215:27;5151:2;5000:258;;;;:::o;5264:320::-;;5345:1;5339:4;5335:12;5325:22;;5392:1;5386:4;5382:12;5413:18;5403:2;;5469:4;5461:6;5457:17;5447:27;;5403:2;5531;5523:6;5520:14;5500:18;5497:38;5494:2;;;5550:18;;:::i;:::-;5494:2;5315:269;;;;:::o;5590:233::-;;5652:24;5670:5;5652:24;:::i;:::-;5643:33;;5698:66;5691:5;5688:77;5685:2;;;5768:18;;:::i;:::-;5685:2;5815:1;5808:5;5804:13;5797:20;;5633:190;;;:::o;5829:180::-;5877:77;5874:1;5867:88;5974:4;5971:1;5964:15;5998:4;5995:1;5988:15;6015:180;6063:77;6060:1;6053:88;6160:4;6157:1;6150:15;6184:4;6181:1;6174:15;6201:180;6249:77;6246:1;6239:88;6346:4;6343:1;6336:15;6370:4;6367:1;6360:15;6387:102;;6479:2;6475:7;6470:2;6463:5;6459:14;6455:28;6445:38;;6435:54;;;:::o;6495:122::-;6568:24;6586:5;6568:24;:::i;:::-;6561:5;6558:35;6548:2;;6607:1;6604;6597:12;6548:2;6538:79;:::o",
  "source": "// SPDX-License-Identifier: MIT\r\npragma solidity >=0.4.22 <0.9.0;\r\n\r\ncontract TasksContract {\r\n\r\n  uint public taskCounter = 0;\r\n\r\n  constructor () {\r\n    createTask(\"Tasks DApp\",  \"Ported to Polyjuice\");\r\n  }\r\n\r\n  struct Task {\r\n    uint256 id;\r\n    string title;\r\n    string description;\r\n    bool done;\r\n    uint256 createdAt;\r\n  }\r\n\r\n  event TaskCreated(\r\n    uint256 id,\r\n    string title,\r\n    string description,\r\n    bool done,\r\n    uint256 createdAt\r\n  );\r\n\r\n  event TaskToggledDone(uint256 id, bool done);\r\n\r\n  mapping (uint256 => Task) public tasks;\r\n\r\n  function createTask(string memory _title, string memory _description) public {\r\n    taskCounter++;\r\n    tasks[taskCounter] = Task(taskCounter, _title, _description, false, block.timestamp);\r\n    emit TaskCreated(taskCounter, _title, _description, false, block.timestamp);\r\n  }\r\n\r\n  function toggleDone(uint256 _id) public {\r\n    Task memory _task = tasks[_id];\r\n    _task.done = !_task.done;\r\n    tasks[_id] = _task;\r\n    emit TaskToggledDone(_id, _task.done);\r\n  }\r\n\r\n}",
  "sourcePath": "/mnt/c/Users/Administrator/Documents/DEV/Proj/Blockchain/ETH_RnD/nervos_bounty_program/gw-gitcoin-instruction/src/examples/2-deploy-contract/contracts/TasksContract.sol",
  "ast": {
    "absolutePath": "project:/contracts/TasksContract.sol",
    "exportedSymbols": {
      "TasksContract": [
        114
      ]
    },
    "id": 115,
    "license": "MIT",
    "nodeType": "SourceUnit",
    "nodes": [
      {
        "id": 1,
        "literals": [
          "solidity",
          ">=",
          "0.4",
          ".22",
          "<",
          "0.9",
          ".0"
        ],
        "nodeType": "PragmaDirective",
        "src": "33:32:0"
      },
      {
        "abstract": false,
        "baseContracts": [],
        "contractDependencies": [],
        "contractKind": "contract",
        "fullyImplemented": true,
        "id": 114,
        "linearizedBaseContracts": [
          114
        ],
        "name": "TasksContract",
        "nodeType": "ContractDefinition",
        "nodes": [
          {
            "constant": false,
            "functionSelector": "58671730",
            "id": 4,
            "mutability": "mutable",
            "name": "taskCounter",
            "nodeType": "VariableDeclaration",
            "scope": 114,
            "src": "99:27:0",
            "stateVariable": true,
            "storageLocation": "default",
            "typeDescriptions": {
              "typeIdentifier": "t_uint256",
              "typeString": "uint256"
            },
            "typeName": {
              "id": 2,
              "name": "uint",
              "nodeType": "ElementaryTypeName",
              "src": "99:4:0",
              "typeDescriptions": {
                "typeIdentifier": "t_uint256",
                "typeString": "uint256"
              }
            },
            "value": {
              "hexValue": "30",
              "id": 3,
              "isConstant": false,
              "isLValue": false,
              "isPure": true,
              "kind": "number",
              "lValueRequested": false,
              "nodeType": "Literal",
              "src": "125:1:0",
              "typeDescriptions": {
                "typeIdentifier": "t_rational_0_by_1",
                "typeString": "int_const 0"
              },
              "value": "0"
            },
            "visibility": "public"
          },
          {
            "body": {
              "id": 12,
              "nodeType": "Block",
              "src": "148:61:0",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "hexValue": "5461736b732044417070",
                        "id": 8,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "string",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "166:12:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_stringliteral_059c2fd482dab936a1a314036cb41fd3d4a274f172abdec924ea367c34fba1aa",
                          "typeString": "literal_string \"Tasks DApp\""
                        },
                        "value": "Tasks DApp"
                      },
                      {
                        "hexValue": "506f7274656420746f20506f6c796a75696365",
                        "id": 9,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "string",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "181:21:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_stringliteral_f76ce3cca9c5bd57b86911457c8fe3b9bbf46ed3f91bfbb0620ef2805a2346d5",
                          "typeString": "literal_string \"Ported to Polyjuice\""
                        },
                        "value": "Ported to Polyjuice"
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_stringliteral_059c2fd482dab936a1a314036cb41fd3d4a274f172abdec924ea367c34fba1aa",
                          "typeString": "literal_string \"Tasks DApp\""
                        },
                        {
                          "typeIdentifier": "t_stringliteral_f76ce3cca9c5bd57b86911457c8fe3b9bbf46ed3f91bfbb0620ef2805a2346d5",
                          "typeString": "literal_string \"Ported to Polyjuice\""
                        }
                      ],
                      "id": 7,
                      "name": "createTask",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 80,
                      "src": "155:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_internal_nonpayable$_t_string_memory_ptr_$_t_string_memory_ptr_$returns$__$",
                        "typeString": "function (string memory,string memory)"
                      }
                    },
                    "id": 10,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "155:48:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 11,
                  "nodeType": "ExpressionStatement",
                  "src": "155:48:0"
                }
              ]
            },
            "id": 13,
            "implemented": true,
            "kind": "constructor",
            "modifiers": [],
            "name": "",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 5,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "145:2:0"
            },
            "returnParameters": {
              "id": 6,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "148:0:0"
            },
            "scope": 114,
            "src": "133:76:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          },
          {
            "canonicalName": "TasksContract.Task",
            "id": 24,
            "members": [
              {
                "constant": false,
                "id": 15,
                "mutability": "mutable",
                "name": "id",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "234:10:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                },
                "typeName": {
                  "id": 14,
                  "name": "uint256",
                  "nodeType": "ElementaryTypeName",
                  "src": "234:7:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 17,
                "mutability": "mutable",
                "name": "title",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "251:12:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_string_storage_ptr",
                  "typeString": "string"
                },
                "typeName": {
                  "id": 16,
                  "name": "string",
                  "nodeType": "ElementaryTypeName",
                  "src": "251:6:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_storage_ptr",
                    "typeString": "string"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 19,
                "mutability": "mutable",
                "name": "description",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "270:18:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_string_storage_ptr",
                  "typeString": "string"
                },
                "typeName": {
                  "id": 18,
                  "name": "string",
                  "nodeType": "ElementaryTypeName",
                  "src": "270:6:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_storage_ptr",
                    "typeString": "string"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 21,
                "mutability": "mutable",
                "name": "done",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "295:9:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_bool",
                  "typeString": "bool"
                },
                "typeName": {
                  "id": 20,
                  "name": "bool",
                  "nodeType": "ElementaryTypeName",
                  "src": "295:4:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 23,
                "mutability": "mutable",
                "name": "createdAt",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "311:17:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                },
                "typeName": {
                  "id": 22,
                  "name": "uint256",
                  "nodeType": "ElementaryTypeName",
                  "src": "311:7:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  }
                },
                "visibility": "internal"
              }
            ],
            "name": "Task",
            "nodeType": "StructDefinition",
            "scope": 114,
            "src": "215:119:0",
            "visibility": "public"
          },
          {
            "anonymous": false,
            "id": 36,
            "name": "TaskCreated",
            "nodeType": "EventDefinition",
            "parameters": {
              "id": 35,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 26,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "id",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "364:10:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 25,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "364:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 28,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "title",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "381:12:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 27,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "381:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 30,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "description",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "400:18:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 29,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "400:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 32,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "done",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "425:9:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  },
                  "typeName": {
                    "id": 31,
                    "name": "bool",
                    "nodeType": "ElementaryTypeName",
                    "src": "425:4:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 34,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "createdAt",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "441:17:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 33,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "441:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "357:106:0"
            },
            "src": "340:124:0"
          },
          {
            "anonymous": false,
            "id": 42,
            "name": "TaskToggledDone",
            "nodeType": "EventDefinition",
            "parameters": {
              "id": 41,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 38,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "id",
                  "nodeType": "VariableDeclaration",
                  "scope": 42,
                  "src": "492:10:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 37,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "492:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 40,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "done",
                  "nodeType": "VariableDeclaration",
                  "scope": 42,
                  "src": "504:9:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  },
                  "typeName": {
                    "id": 39,
                    "name": "bool",
                    "nodeType": "ElementaryTypeName",
                    "src": "504:4:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "491:23:0"
            },
            "src": "470:45:0"
          },
          {
            "constant": false,
            "functionSelector": "8d977672",
            "id": 47,
            "mutability": "mutable",
            "name": "tasks",
            "nodeType": "VariableDeclaration",
            "scope": 114,
            "src": "521:38:0",
            "stateVariable": true,
            "storageLocation": "default",
            "typeDescriptions": {
              "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
              "typeString": "mapping(uint256 => struct TasksContract.Task)"
            },
            "typeName": {
              "id": 46,
              "keyType": {
                "id": 43,
                "name": "uint256",
                "nodeType": "ElementaryTypeName",
                "src": "530:7:0",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                }
              },
              "nodeType": "Mapping",
              "src": "521:25:0",
              "typeDescriptions": {
                "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                "typeString": "mapping(uint256 => struct TasksContract.Task)"
              },
              "valueType": {
                "id": 45,
                "nodeType": "UserDefinedTypeName",
                "pathNode": {
                  "id": 44,
                  "name": "Task",
                  "nodeType": "IdentifierPath",
                  "referencedDeclaration": 24,
                  "src": "541:4:0"
                },
                "referencedDeclaration": 24,
                "src": "541:4:0",
                "typeDescriptions": {
                  "typeIdentifier": "t_struct$_Task_$24_storage_ptr",
                  "typeString": "struct TasksContract.Task"
                }
              }
            },
            "visibility": "public"
          },
          {
            "body": {
              "id": 79,
              "nodeType": "Block",
              "src": "643:199:0",
              "statements": [
                {
                  "expression": {
                    "id": 55,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "nodeType": "UnaryOperation",
                    "operator": "++",
                    "prefix": false,
                    "src": "650:13:0",
                    "subExpression": {
                      "id": 54,
                      "name": "taskCounter",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 4,
                      "src": "650:11:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_uint256",
                        "typeString": "uint256"
                      }
                    },
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "id": 56,
                  "nodeType": "ExpressionStatement",
                  "src": "650:13:0"
                },
                {
                  "expression": {
                    "id": 68,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "baseExpression": {
                        "id": 57,
                        "name": "tasks",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 47,
                        "src": "670:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                          "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                        }
                      },
                      "id": 59,
                      "indexExpression": {
                        "id": 58,
                        "name": "taskCounter",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 4,
                        "src": "676:11:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "nodeType": "IndexAccess",
                      "src": "670:18:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_storage",
                        "typeString": "struct TasksContract.Task storage ref"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "arguments": [
                        {
                          "id": 61,
                          "name": "taskCounter",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 4,
                          "src": "696:11:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        },
                        {
                          "id": 62,
                          "name": "_title",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 49,
                          "src": "709:6:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          }
                        },
                        {
                          "id": 63,
                          "name": "_description",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 51,
                          "src": "717:12:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          }
                        },
                        {
                          "hexValue": "66616c7365",
                          "id": 64,
                          "isConstant": false,
                          "isLValue": false,
                          "isPure": true,
                          "kind": "bool",
                          "lValueRequested": false,
                          "nodeType": "Literal",
                          "src": "731:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_bool",
                            "typeString": "bool"
                          },
                          "value": "false"
                        },
                        {
                          "expression": {
                            "id": 65,
                            "name": "block",
                            "nodeType": "Identifier",
                            "overloadedDeclarations": [],
                            "referencedDeclaration": 4294967292,
                            "src": "738:5:0",
                            "typeDescriptions": {
                              "typeIdentifier": "t_magic_block",
                              "typeString": "block"
                            }
                          },
                          "id": 66,
                          "isConstant": false,
                          "isLValue": false,
                          "isPure": false,
                          "lValueRequested": false,
                          "memberName": "timestamp",
                          "nodeType": "MemberAccess",
                          "src": "738:15:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        }
                      ],
                      "expression": {
                        "argumentTypes": [
                          {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          },
                          {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          },
                          {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          },
                          {
                            "typeIdentifier": "t_bool",
                            "typeString": "bool"
                          },
                          {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        ],
                        "id": 60,
                        "name": "Task",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 24,
                        "src": "691:4:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_type$_t_struct$_Task_$24_storage_ptr_$",
                          "typeString": "type(struct TasksContract.Task storage pointer)"
                        }
                      },
                      "id": 67,
                      "isConstant": false,
                      "isLValue": false,
                      "isPure": false,
                      "kind": "structConstructorCall",
                      "lValueRequested": false,
                      "names": [],
                      "nodeType": "FunctionCall",
                      "src": "691:63:0",
                      "tryCall": false,
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task memory"
                      }
                    },
                    "src": "670:84:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "id": 69,
                  "nodeType": "ExpressionStatement",
                  "src": "670:84:0"
                },
                {
                  "eventCall": {
                    "arguments": [
                      {
                        "id": 71,
                        "name": "taskCounter",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 4,
                        "src": "778:11:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      {
                        "id": 72,
                        "name": "_title",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 49,
                        "src": "791:6:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        }
                      },
                      {
                        "id": 73,
                        "name": "_description",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 51,
                        "src": "799:12:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        }
                      },
                      {
                        "hexValue": "66616c7365",
                        "id": 74,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "bool",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "813:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        },
                        "value": "false"
                      },
                      {
                        "expression": {
                          "id": 75,
                          "name": "block",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 4294967292,
                          "src": "820:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_magic_block",
                            "typeString": "block"
                          }
                        },
                        "id": 76,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "timestamp",
                        "nodeType": "MemberAccess",
                        "src": "820:15:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        },
                        {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        },
                        {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        },
                        {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        },
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      ],
                      "id": 70,
                      "name": "TaskCreated",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 36,
                      "src": "766:11:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_event_nonpayable$_t_uint256_$_t_string_memory_ptr_$_t_string_memory_ptr_$_t_bool_$_t_uint256_$returns$__$",
                        "typeString": "function (uint256,string memory,string memory,bool,uint256)"
                      }
                    },
                    "id": 77,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "766:70:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 78,
                  "nodeType": "EmitStatement",
                  "src": "761:75:0"
                }
              ]
            },
            "functionSelector": "292a4585",
            "id": 80,
            "implemented": true,
            "kind": "function",
            "modifiers": [],
            "name": "createTask",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 52,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 49,
                  "mutability": "mutable",
                  "name": "_title",
                  "nodeType": "VariableDeclaration",
                  "scope": 80,
                  "src": "586:20:0",
                  "stateVariable": false,
                  "storageLocation": "memory",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 48,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "586:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 51,
                  "mutability": "mutable",
                  "name": "_description",
                  "nodeType": "VariableDeclaration",
                  "scope": 80,
                  "src": "608:26:0",
                  "stateVariable": false,
                  "storageLocation": "memory",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 50,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "608:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "585:50:0"
            },
            "returnParameters": {
              "id": 53,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "643:0:0"
            },
            "scope": 114,
            "src": "566:276:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          },
          {
            "body": {
              "id": 112,
              "nodeType": "Block",
              "src": "888:143:0",
              "statements": [
                {
                  "assignments": [
                    87
                  ],
                  "declarations": [
                    {
                      "constant": false,
                      "id": 87,
                      "mutability": "mutable",
                      "name": "_task",
                      "nodeType": "VariableDeclaration",
                      "scope": 112,
                      "src": "895:17:0",
                      "stateVariable": false,
                      "storageLocation": "memory",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task"
                      },
                      "typeName": {
                        "id": 86,
                        "nodeType": "UserDefinedTypeName",
                        "pathNode": {
                          "id": 85,
                          "name": "Task",
                          "nodeType": "IdentifierPath",
                          "referencedDeclaration": 24,
                          "src": "895:4:0"
                        },
                        "referencedDeclaration": 24,
                        "src": "895:4:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_struct$_Task_$24_storage_ptr",
                          "typeString": "struct TasksContract.Task"
                        }
                      },
                      "visibility": "internal"
                    }
                  ],
                  "id": 91,
                  "initialValue": {
                    "baseExpression": {
                      "id": 88,
                      "name": "tasks",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 47,
                      "src": "915:5:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                        "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                      }
                    },
                    "id": 90,
                    "indexExpression": {
                      "id": 89,
                      "name": "_id",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 82,
                      "src": "921:3:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_uint256",
                        "typeString": "uint256"
                      }
                    },
                    "isConstant": false,
                    "isLValue": true,
                    "isPure": false,
                    "lValueRequested": false,
                    "nodeType": "IndexAccess",
                    "src": "915:10:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "nodeType": "VariableDeclarationStatement",
                  "src": "895:30:0"
                },
                {
                  "expression": {
                    "id": 98,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "expression": {
                        "id": 92,
                        "name": "_task",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 87,
                        "src": "932:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                          "typeString": "struct TasksContract.Task memory"
                        }
                      },
                      "id": 94,
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "memberName": "done",
                      "nodeType": "MemberAccess",
                      "referencedDeclaration": 21,
                      "src": "932:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_bool",
                        "typeString": "bool"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "id": 97,
                      "isConstant": false,
                      "isLValue": false,
                      "isPure": false,
                      "lValueRequested": false,
                      "nodeType": "UnaryOperation",
                      "operator": "!",
                      "prefix": true,
                      "src": "945:11:0",
                      "subExpression": {
                        "expression": {
                          "id": 95,
                          "name": "_task",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 87,
                          "src": "946:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                            "typeString": "struct TasksContract.Task memory"
                          }
                        },
                        "id": 96,
                        "isConstant": false,
                        "isLValue": true,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "done",
                        "nodeType": "MemberAccess",
                        "referencedDeclaration": 21,
                        "src": "946:10:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      },
                      "typeDescriptions": {
                        "typeIdentifier": "t_bool",
                        "typeString": "bool"
                      }
                    },
                    "src": "932:24:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "id": 99,
                  "nodeType": "ExpressionStatement",
                  "src": "932:24:0"
                },
                {
                  "expression": {
                    "id": 104,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "baseExpression": {
                        "id": 100,
                        "name": "tasks",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 47,
                        "src": "963:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                          "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                        }
                      },
                      "id": 102,
                      "indexExpression": {
                        "id": 101,
                        "name": "_id",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 82,
                        "src": "969:3:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "nodeType": "IndexAccess",
                      "src": "963:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_storage",
                        "typeString": "struct TasksContract.Task storage ref"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "id": 103,
                      "name": "_task",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 87,
                      "src": "976:5:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task memory"
                      }
                    },
                    "src": "963:18:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "id": 105,
                  "nodeType": "ExpressionStatement",
                  "src": "963:18:0"
                },
                {
                  "eventCall": {
                    "arguments": [
                      {
                        "id": 107,
                        "name": "_id",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 82,
                        "src": "1009:3:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      {
                        "expression": {
                          "id": 108,
                          "name": "_task",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 87,
                          "src": "1014:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                            "typeString": "struct TasksContract.Task memory"
                          }
                        },
                        "id": 109,
                        "isConstant": false,
                        "isLValue": true,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "done",
                        "nodeType": "MemberAccess",
                        "referencedDeclaration": 21,
                        "src": "1014:10:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        },
                        {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      ],
                      "id": 106,
                      "name": "TaskToggledDone",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 42,
                      "src": "993:15:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_event_nonpayable$_t_uint256_$_t_bool_$returns$__$",
                        "typeString": "function (uint256,bool)"
                      }
                    },
                    "id": 110,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "993:32:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 111,
                  "nodeType": "EmitStatement",
                  "src": "988:37:0"
                }
              ]
            },
            "functionSelector": "d81ef739",
            "id": 113,
            "implemented": true,
            "kind": "function",
            "modifiers": [],
            "name": "toggleDone",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 83,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 82,
                  "mutability": "mutable",
                  "name": "_id",
                  "nodeType": "VariableDeclaration",
                  "scope": 113,
                  "src": "868:11:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 81,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "868:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "867:13:0"
            },
            "returnParameters": {
              "id": 84,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "888:0:0"
            },
            "scope": 114,
            "src": "848:183:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          }
        ],
        "scope": 115,
        "src": "69:967:0"
      }
    ],
    "src": "33:1003:0"
  },
  "legacyAST": {
    "absolutePath": "project:/contracts/TasksContract.sol",
    "exportedSymbols": {
      "TasksContract": [
        114
      ]
    },
    "id": 115,
    "license": "MIT",
    "nodeType": "SourceUnit",
    "nodes": [
      {
        "id": 1,
        "literals": [
          "solidity",
          ">=",
          "0.4",
          ".22",
          "<",
          "0.9",
          ".0"
        ],
        "nodeType": "PragmaDirective",
        "src": "33:32:0"
      },
      {
        "abstract": false,
        "baseContracts": [],
        "contractDependencies": [],
        "contractKind": "contract",
        "fullyImplemented": true,
        "id": 114,
        "linearizedBaseContracts": [
          114
        ],
        "name": "TasksContract",
        "nodeType": "ContractDefinition",
        "nodes": [
          {
            "constant": false,
            "functionSelector": "58671730",
            "id": 4,
            "mutability": "mutable",
            "name": "taskCounter",
            "nodeType": "VariableDeclaration",
            "scope": 114,
            "src": "99:27:0",
            "stateVariable": true,
            "storageLocation": "default",
            "typeDescriptions": {
              "typeIdentifier": "t_uint256",
              "typeString": "uint256"
            },
            "typeName": {
              "id": 2,
              "name": "uint",
              "nodeType": "ElementaryTypeName",
              "src": "99:4:0",
              "typeDescriptions": {
                "typeIdentifier": "t_uint256",
                "typeString": "uint256"
              }
            },
            "value": {
              "hexValue": "30",
              "id": 3,
              "isConstant": false,
              "isLValue": false,
              "isPure": true,
              "kind": "number",
              "lValueRequested": false,
              "nodeType": "Literal",
              "src": "125:1:0",
              "typeDescriptions": {
                "typeIdentifier": "t_rational_0_by_1",
                "typeString": "int_const 0"
              },
              "value": "0"
            },
            "visibility": "public"
          },
          {
            "body": {
              "id": 12,
              "nodeType": "Block",
              "src": "148:61:0",
              "statements": [
                {
                  "expression": {
                    "arguments": [
                      {
                        "hexValue": "5461736b732044417070",
                        "id": 8,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "string",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "166:12:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_stringliteral_059c2fd482dab936a1a314036cb41fd3d4a274f172abdec924ea367c34fba1aa",
                          "typeString": "literal_string \"Tasks DApp\""
                        },
                        "value": "Tasks DApp"
                      },
                      {
                        "hexValue": "506f7274656420746f20506f6c796a75696365",
                        "id": 9,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "string",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "181:21:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_stringliteral_f76ce3cca9c5bd57b86911457c8fe3b9bbf46ed3f91bfbb0620ef2805a2346d5",
                          "typeString": "literal_string \"Ported to Polyjuice\""
                        },
                        "value": "Ported to Polyjuice"
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_stringliteral_059c2fd482dab936a1a314036cb41fd3d4a274f172abdec924ea367c34fba1aa",
                          "typeString": "literal_string \"Tasks DApp\""
                        },
                        {
                          "typeIdentifier": "t_stringliteral_f76ce3cca9c5bd57b86911457c8fe3b9bbf46ed3f91bfbb0620ef2805a2346d5",
                          "typeString": "literal_string \"Ported to Polyjuice\""
                        }
                      ],
                      "id": 7,
                      "name": "createTask",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 80,
                      "src": "155:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_internal_nonpayable$_t_string_memory_ptr_$_t_string_memory_ptr_$returns$__$",
                        "typeString": "function (string memory,string memory)"
                      }
                    },
                    "id": 10,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "155:48:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 11,
                  "nodeType": "ExpressionStatement",
                  "src": "155:48:0"
                }
              ]
            },
            "id": 13,
            "implemented": true,
            "kind": "constructor",
            "modifiers": [],
            "name": "",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 5,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "145:2:0"
            },
            "returnParameters": {
              "id": 6,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "148:0:0"
            },
            "scope": 114,
            "src": "133:76:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          },
          {
            "canonicalName": "TasksContract.Task",
            "id": 24,
            "members": [
              {
                "constant": false,
                "id": 15,
                "mutability": "mutable",
                "name": "id",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "234:10:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                },
                "typeName": {
                  "id": 14,
                  "name": "uint256",
                  "nodeType": "ElementaryTypeName",
                  "src": "234:7:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 17,
                "mutability": "mutable",
                "name": "title",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "251:12:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_string_storage_ptr",
                  "typeString": "string"
                },
                "typeName": {
                  "id": 16,
                  "name": "string",
                  "nodeType": "ElementaryTypeName",
                  "src": "251:6:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_storage_ptr",
                    "typeString": "string"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 19,
                "mutability": "mutable",
                "name": "description",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "270:18:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_string_storage_ptr",
                  "typeString": "string"
                },
                "typeName": {
                  "id": 18,
                  "name": "string",
                  "nodeType": "ElementaryTypeName",
                  "src": "270:6:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_storage_ptr",
                    "typeString": "string"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 21,
                "mutability": "mutable",
                "name": "done",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "295:9:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_bool",
                  "typeString": "bool"
                },
                "typeName": {
                  "id": 20,
                  "name": "bool",
                  "nodeType": "ElementaryTypeName",
                  "src": "295:4:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  }
                },
                "visibility": "internal"
              },
              {
                "constant": false,
                "id": 23,
                "mutability": "mutable",
                "name": "createdAt",
                "nodeType": "VariableDeclaration",
                "scope": 24,
                "src": "311:17:0",
                "stateVariable": false,
                "storageLocation": "default",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                },
                "typeName": {
                  "id": 22,
                  "name": "uint256",
                  "nodeType": "ElementaryTypeName",
                  "src": "311:7:0",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  }
                },
                "visibility": "internal"
              }
            ],
            "name": "Task",
            "nodeType": "StructDefinition",
            "scope": 114,
            "src": "215:119:0",
            "visibility": "public"
          },
          {
            "anonymous": false,
            "id": 36,
            "name": "TaskCreated",
            "nodeType": "EventDefinition",
            "parameters": {
              "id": 35,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 26,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "id",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "364:10:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 25,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "364:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 28,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "title",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "381:12:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 27,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "381:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 30,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "description",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "400:18:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 29,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "400:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 32,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "done",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "425:9:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  },
                  "typeName": {
                    "id": 31,
                    "name": "bool",
                    "nodeType": "ElementaryTypeName",
                    "src": "425:4:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 34,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "createdAt",
                  "nodeType": "VariableDeclaration",
                  "scope": 36,
                  "src": "441:17:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 33,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "441:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "357:106:0"
            },
            "src": "340:124:0"
          },
          {
            "anonymous": false,
            "id": 42,
            "name": "TaskToggledDone",
            "nodeType": "EventDefinition",
            "parameters": {
              "id": 41,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 38,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "id",
                  "nodeType": "VariableDeclaration",
                  "scope": 42,
                  "src": "492:10:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 37,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "492:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 40,
                  "indexed": false,
                  "mutability": "mutable",
                  "name": "done",
                  "nodeType": "VariableDeclaration",
                  "scope": 42,
                  "src": "504:9:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_bool",
                    "typeString": "bool"
                  },
                  "typeName": {
                    "id": 39,
                    "name": "bool",
                    "nodeType": "ElementaryTypeName",
                    "src": "504:4:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "491:23:0"
            },
            "src": "470:45:0"
          },
          {
            "constant": false,
            "functionSelector": "8d977672",
            "id": 47,
            "mutability": "mutable",
            "name": "tasks",
            "nodeType": "VariableDeclaration",
            "scope": 114,
            "src": "521:38:0",
            "stateVariable": true,
            "storageLocation": "default",
            "typeDescriptions": {
              "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
              "typeString": "mapping(uint256 => struct TasksContract.Task)"
            },
            "typeName": {
              "id": 46,
              "keyType": {
                "id": 43,
                "name": "uint256",
                "nodeType": "ElementaryTypeName",
                "src": "530:7:0",
                "typeDescriptions": {
                  "typeIdentifier": "t_uint256",
                  "typeString": "uint256"
                }
              },
              "nodeType": "Mapping",
              "src": "521:25:0",
              "typeDescriptions": {
                "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                "typeString": "mapping(uint256 => struct TasksContract.Task)"
              },
              "valueType": {
                "id": 45,
                "nodeType": "UserDefinedTypeName",
                "pathNode": {
                  "id": 44,
                  "name": "Task",
                  "nodeType": "IdentifierPath",
                  "referencedDeclaration": 24,
                  "src": "541:4:0"
                },
                "referencedDeclaration": 24,
                "src": "541:4:0",
                "typeDescriptions": {
                  "typeIdentifier": "t_struct$_Task_$24_storage_ptr",
                  "typeString": "struct TasksContract.Task"
                }
              }
            },
            "visibility": "public"
          },
          {
            "body": {
              "id": 79,
              "nodeType": "Block",
              "src": "643:199:0",
              "statements": [
                {
                  "expression": {
                    "id": 55,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "nodeType": "UnaryOperation",
                    "operator": "++",
                    "prefix": false,
                    "src": "650:13:0",
                    "subExpression": {
                      "id": 54,
                      "name": "taskCounter",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 4,
                      "src": "650:11:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_uint256",
                        "typeString": "uint256"
                      }
                    },
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "id": 56,
                  "nodeType": "ExpressionStatement",
                  "src": "650:13:0"
                },
                {
                  "expression": {
                    "id": 68,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "baseExpression": {
                        "id": 57,
                        "name": "tasks",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 47,
                        "src": "670:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                          "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                        }
                      },
                      "id": 59,
                      "indexExpression": {
                        "id": 58,
                        "name": "taskCounter",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 4,
                        "src": "676:11:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "nodeType": "IndexAccess",
                      "src": "670:18:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_storage",
                        "typeString": "struct TasksContract.Task storage ref"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "arguments": [
                        {
                          "id": 61,
                          "name": "taskCounter",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 4,
                          "src": "696:11:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        },
                        {
                          "id": 62,
                          "name": "_title",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 49,
                          "src": "709:6:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          }
                        },
                        {
                          "id": 63,
                          "name": "_description",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 51,
                          "src": "717:12:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          }
                        },
                        {
                          "hexValue": "66616c7365",
                          "id": 64,
                          "isConstant": false,
                          "isLValue": false,
                          "isPure": true,
                          "kind": "bool",
                          "lValueRequested": false,
                          "nodeType": "Literal",
                          "src": "731:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_bool",
                            "typeString": "bool"
                          },
                          "value": "false"
                        },
                        {
                          "expression": {
                            "id": 65,
                            "name": "block",
                            "nodeType": "Identifier",
                            "overloadedDeclarations": [],
                            "referencedDeclaration": 4294967292,
                            "src": "738:5:0",
                            "typeDescriptions": {
                              "typeIdentifier": "t_magic_block",
                              "typeString": "block"
                            }
                          },
                          "id": 66,
                          "isConstant": false,
                          "isLValue": false,
                          "isPure": false,
                          "lValueRequested": false,
                          "memberName": "timestamp",
                          "nodeType": "MemberAccess",
                          "src": "738:15:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        }
                      ],
                      "expression": {
                        "argumentTypes": [
                          {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          },
                          {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          },
                          {
                            "typeIdentifier": "t_string_memory_ptr",
                            "typeString": "string memory"
                          },
                          {
                            "typeIdentifier": "t_bool",
                            "typeString": "bool"
                          },
                          {
                            "typeIdentifier": "t_uint256",
                            "typeString": "uint256"
                          }
                        ],
                        "id": 60,
                        "name": "Task",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 24,
                        "src": "691:4:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_type$_t_struct$_Task_$24_storage_ptr_$",
                          "typeString": "type(struct TasksContract.Task storage pointer)"
                        }
                      },
                      "id": 67,
                      "isConstant": false,
                      "isLValue": false,
                      "isPure": false,
                      "kind": "structConstructorCall",
                      "lValueRequested": false,
                      "names": [],
                      "nodeType": "FunctionCall",
                      "src": "691:63:0",
                      "tryCall": false,
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task memory"
                      }
                    },
                    "src": "670:84:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "id": 69,
                  "nodeType": "ExpressionStatement",
                  "src": "670:84:0"
                },
                {
                  "eventCall": {
                    "arguments": [
                      {
                        "id": 71,
                        "name": "taskCounter",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 4,
                        "src": "778:11:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      {
                        "id": 72,
                        "name": "_title",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 49,
                        "src": "791:6:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        }
                      },
                      {
                        "id": 73,
                        "name": "_description",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 51,
                        "src": "799:12:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        }
                      },
                      {
                        "hexValue": "66616c7365",
                        "id": 74,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": true,
                        "kind": "bool",
                        "lValueRequested": false,
                        "nodeType": "Literal",
                        "src": "813:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        },
                        "value": "false"
                      },
                      {
                        "expression": {
                          "id": 75,
                          "name": "block",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 4294967292,
                          "src": "820:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_magic_block",
                            "typeString": "block"
                          }
                        },
                        "id": 76,
                        "isConstant": false,
                        "isLValue": false,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "timestamp",
                        "nodeType": "MemberAccess",
                        "src": "820:15:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        },
                        {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        },
                        {
                          "typeIdentifier": "t_string_memory_ptr",
                          "typeString": "string memory"
                        },
                        {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        },
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      ],
                      "id": 70,
                      "name": "TaskCreated",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 36,
                      "src": "766:11:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_event_nonpayable$_t_uint256_$_t_string_memory_ptr_$_t_string_memory_ptr_$_t_bool_$_t_uint256_$returns$__$",
                        "typeString": "function (uint256,string memory,string memory,bool,uint256)"
                      }
                    },
                    "id": 77,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "766:70:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 78,
                  "nodeType": "EmitStatement",
                  "src": "761:75:0"
                }
              ]
            },
            "functionSelector": "292a4585",
            "id": 80,
            "implemented": true,
            "kind": "function",
            "modifiers": [],
            "name": "createTask",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 52,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 49,
                  "mutability": "mutable",
                  "name": "_title",
                  "nodeType": "VariableDeclaration",
                  "scope": 80,
                  "src": "586:20:0",
                  "stateVariable": false,
                  "storageLocation": "memory",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 48,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "586:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                },
                {
                  "constant": false,
                  "id": 51,
                  "mutability": "mutable",
                  "name": "_description",
                  "nodeType": "VariableDeclaration",
                  "scope": 80,
                  "src": "608:26:0",
                  "stateVariable": false,
                  "storageLocation": "memory",
                  "typeDescriptions": {
                    "typeIdentifier": "t_string_memory_ptr",
                    "typeString": "string"
                  },
                  "typeName": {
                    "id": 50,
                    "name": "string",
                    "nodeType": "ElementaryTypeName",
                    "src": "608:6:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_string_storage_ptr",
                      "typeString": "string"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "585:50:0"
            },
            "returnParameters": {
              "id": 53,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "643:0:0"
            },
            "scope": 114,
            "src": "566:276:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          },
          {
            "body": {
              "id": 112,
              "nodeType": "Block",
              "src": "888:143:0",
              "statements": [
                {
                  "assignments": [
                    87
                  ],
                  "declarations": [
                    {
                      "constant": false,
                      "id": 87,
                      "mutability": "mutable",
                      "name": "_task",
                      "nodeType": "VariableDeclaration",
                      "scope": 112,
                      "src": "895:17:0",
                      "stateVariable": false,
                      "storageLocation": "memory",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task"
                      },
                      "typeName": {
                        "id": 86,
                        "nodeType": "UserDefinedTypeName",
                        "pathNode": {
                          "id": 85,
                          "name": "Task",
                          "nodeType": "IdentifierPath",
                          "referencedDeclaration": 24,
                          "src": "895:4:0"
                        },
                        "referencedDeclaration": 24,
                        "src": "895:4:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_struct$_Task_$24_storage_ptr",
                          "typeString": "struct TasksContract.Task"
                        }
                      },
                      "visibility": "internal"
                    }
                  ],
                  "id": 91,
                  "initialValue": {
                    "baseExpression": {
                      "id": 88,
                      "name": "tasks",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 47,
                      "src": "915:5:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                        "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                      }
                    },
                    "id": 90,
                    "indexExpression": {
                      "id": 89,
                      "name": "_id",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 82,
                      "src": "921:3:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_uint256",
                        "typeString": "uint256"
                      }
                    },
                    "isConstant": false,
                    "isLValue": true,
                    "isPure": false,
                    "lValueRequested": false,
                    "nodeType": "IndexAccess",
                    "src": "915:10:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "nodeType": "VariableDeclarationStatement",
                  "src": "895:30:0"
                },
                {
                  "expression": {
                    "id": 98,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "expression": {
                        "id": 92,
                        "name": "_task",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 87,
                        "src": "932:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                          "typeString": "struct TasksContract.Task memory"
                        }
                      },
                      "id": 94,
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "memberName": "done",
                      "nodeType": "MemberAccess",
                      "referencedDeclaration": 21,
                      "src": "932:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_bool",
                        "typeString": "bool"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "id": 97,
                      "isConstant": false,
                      "isLValue": false,
                      "isPure": false,
                      "lValueRequested": false,
                      "nodeType": "UnaryOperation",
                      "operator": "!",
                      "prefix": true,
                      "src": "945:11:0",
                      "subExpression": {
                        "expression": {
                          "id": 95,
                          "name": "_task",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 87,
                          "src": "946:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                            "typeString": "struct TasksContract.Task memory"
                          }
                        },
                        "id": 96,
                        "isConstant": false,
                        "isLValue": true,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "done",
                        "nodeType": "MemberAccess",
                        "referencedDeclaration": 21,
                        "src": "946:10:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      },
                      "typeDescriptions": {
                        "typeIdentifier": "t_bool",
                        "typeString": "bool"
                      }
                    },
                    "src": "932:24:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_bool",
                      "typeString": "bool"
                    }
                  },
                  "id": 99,
                  "nodeType": "ExpressionStatement",
                  "src": "932:24:0"
                },
                {
                  "expression": {
                    "id": 104,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "lValueRequested": false,
                    "leftHandSide": {
                      "baseExpression": {
                        "id": 100,
                        "name": "tasks",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 47,
                        "src": "963:5:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_mapping$_t_uint256_$_t_struct$_Task_$24_storage_$",
                          "typeString": "mapping(uint256 => struct TasksContract.Task storage ref)"
                        }
                      },
                      "id": 102,
                      "indexExpression": {
                        "id": 101,
                        "name": "_id",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 82,
                        "src": "969:3:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      "isConstant": false,
                      "isLValue": true,
                      "isPure": false,
                      "lValueRequested": true,
                      "nodeType": "IndexAccess",
                      "src": "963:10:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_storage",
                        "typeString": "struct TasksContract.Task storage ref"
                      }
                    },
                    "nodeType": "Assignment",
                    "operator": "=",
                    "rightHandSide": {
                      "id": 103,
                      "name": "_task",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 87,
                      "src": "976:5:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                        "typeString": "struct TasksContract.Task memory"
                      }
                    },
                    "src": "963:18:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_struct$_Task_$24_storage",
                      "typeString": "struct TasksContract.Task storage ref"
                    }
                  },
                  "id": 105,
                  "nodeType": "ExpressionStatement",
                  "src": "963:18:0"
                },
                {
                  "eventCall": {
                    "arguments": [
                      {
                        "id": 107,
                        "name": "_id",
                        "nodeType": "Identifier",
                        "overloadedDeclarations": [],
                        "referencedDeclaration": 82,
                        "src": "1009:3:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        }
                      },
                      {
                        "expression": {
                          "id": 108,
                          "name": "_task",
                          "nodeType": "Identifier",
                          "overloadedDeclarations": [],
                          "referencedDeclaration": 87,
                          "src": "1014:5:0",
                          "typeDescriptions": {
                            "typeIdentifier": "t_struct$_Task_$24_memory_ptr",
                            "typeString": "struct TasksContract.Task memory"
                          }
                        },
                        "id": 109,
                        "isConstant": false,
                        "isLValue": true,
                        "isPure": false,
                        "lValueRequested": false,
                        "memberName": "done",
                        "nodeType": "MemberAccess",
                        "referencedDeclaration": 21,
                        "src": "1014:10:0",
                        "typeDescriptions": {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      }
                    ],
                    "expression": {
                      "argumentTypes": [
                        {
                          "typeIdentifier": "t_uint256",
                          "typeString": "uint256"
                        },
                        {
                          "typeIdentifier": "t_bool",
                          "typeString": "bool"
                        }
                      ],
                      "id": 106,
                      "name": "TaskToggledDone",
                      "nodeType": "Identifier",
                      "overloadedDeclarations": [],
                      "referencedDeclaration": 42,
                      "src": "993:15:0",
                      "typeDescriptions": {
                        "typeIdentifier": "t_function_event_nonpayable$_t_uint256_$_t_bool_$returns$__$",
                        "typeString": "function (uint256,bool)"
                      }
                    },
                    "id": 110,
                    "isConstant": false,
                    "isLValue": false,
                    "isPure": false,
                    "kind": "functionCall",
                    "lValueRequested": false,
                    "names": [],
                    "nodeType": "FunctionCall",
                    "src": "993:32:0",
                    "tryCall": false,
                    "typeDescriptions": {
                      "typeIdentifier": "t_tuple$__$",
                      "typeString": "tuple()"
                    }
                  },
                  "id": 111,
                  "nodeType": "EmitStatement",
                  "src": "988:37:0"
                }
              ]
            },
            "functionSelector": "d81ef739",
            "id": 113,
            "implemented": true,
            "kind": "function",
            "modifiers": [],
            "name": "toggleDone",
            "nodeType": "FunctionDefinition",
            "parameters": {
              "id": 83,
              "nodeType": "ParameterList",
              "parameters": [
                {
                  "constant": false,
                  "id": 82,
                  "mutability": "mutable",
                  "name": "_id",
                  "nodeType": "VariableDeclaration",
                  "scope": 113,
                  "src": "868:11:0",
                  "stateVariable": false,
                  "storageLocation": "default",
                  "typeDescriptions": {
                    "typeIdentifier": "t_uint256",
                    "typeString": "uint256"
                  },
                  "typeName": {
                    "id": 81,
                    "name": "uint256",
                    "nodeType": "ElementaryTypeName",
                    "src": "868:7:0",
                    "typeDescriptions": {
                      "typeIdentifier": "t_uint256",
                      "typeString": "uint256"
                    }
                  },
                  "visibility": "internal"
                }
              ],
              "src": "867:13:0"
            },
            "returnParameters": {
              "id": 84,
              "nodeType": "ParameterList",
              "parameters": [],
              "src": "888:0:0"
            },
            "scope": 114,
            "src": "848:183:0",
            "stateMutability": "nonpayable",
            "virtual": false,
            "visibility": "public"
          }
        ],
        "scope": 115,
        "src": "69:967:0"
      }
    ],
    "src": "33:1003:0"
  },
  "compiler": {
    "name": "solc",
    "version": "0.8.0+commit.c7dfd78e.Emscripten.clang"
  },
  "networks": {
    "5777": {
      "events": {},
      "links": {},
      "address": "0x760bEB19b6eD3833cF6EC52CDb5b78D3E74f75d1",
      "transactionHash": "0x369e5e7d4ea95013aa8c6596e919ad27d54c9e49c805047a2c6c745a490fe908"
    },
    "71393": {
      "events": {
        "0x6549102bed7d1bb5ec529ee14e2ca60ffc1f47f66d4cc6ca713220613cc64c25": {
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
        "0x3a359256e016dcfa8426ec503e08484999d6fcfb8c0f6084dc9e63374d838429": {
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
        }
      },
      "links": {},
      "address": "0x17148DC771e7192701afB2c54F70E47651b479E3",
      "transactionHash": "0xfbb9e98f94325179d47459334dfa2814a316269a52f42928f6a630b3af9a1cfc"
    }
  },
  "schemaVersion": "3.4.2",
  "updatedAt": "2021-08-14T11:57:13.463Z",
  "devdoc": {
    "kind": "dev",
    "methods": {},
    "version": 1
  },
  "userdoc": {
    "kind": "user",
    "methods": {},
    "version": 1
  }
}
