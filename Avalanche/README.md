## Avalanche | Avalanche: A Network of Networks with

Task : Gain a high-level understanding of Avalanche's Network architecture, Subnet deployment, and potentially a Teleporter bridge deployment.

avalanche subnet deploy mysubnet

![alt text](imagen.png)

![alt text](imagen-1.png)

![alt text](imagen-2.png)


valanche subnet describe mysubnet

![alt text](imagen-3.png)

![alt text](imagen-4.png)

![alt text](imagen-5.png)

![alt text](imagen-6.png)

![alt text](imagen-7.png)


forge create --rpc-url local-c --private-key $PK src/0-send-receive/senderOnCChain.sol:SenderOnCChain

![alt text](imagen-8.png)



forge create --rpc-url mysubnet --private-key $PK src/0-send-receive/receiverOnSubnet.sol:ReceiverOnSubnet

![alt text](imagen-9.png)


cast send --rpc-url local-c --private-key $PK <sender_contract_address> "sendMessage(address,string)" <receiver_contract_address> "Hello"

![alt text](imagen-10.png)