This is a submission for the Daksh’18 Hackathon by Guvi. <br>
This project is an amalgamation of two very different modules.<br>
One of the module uses Python exclusively with Flask-API and the other is an ethereum smart contract that runs on Node.js and Soilidity
Please follow these steps religiously<br><br>
Step 1 - Git clone this rep<br>
Step 2 - Open Command prompt/ Terminal and type in this<br>
		pip install -r requirements.txt<br>
Step 3 - python app.py<br>
Step 4 - Open a new terminal, type in node then npm install ethereumjs-testrpc web3<br>
Step 5 - npm install solc<br>
Step 6 - Go to node_modules/.bin/testrpc and run testrpc<br>
Step 7 - Open a new terminal (again..) and give these commands from node terminal<br>
node<br>
> Web3 = require('web3')<br>
> web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));<br>
> web3.eth.accounts<br>
> code = fs.readFileSync('Voting.sol').toString()<br>
> solc = require('solc')<br>
> compiledCode = solc.compile(code)<br>
> abiDefinition = JSON.parse(compiledCode.contracts[':Voting'].interface)<br>
> VotingContract = web3.eth.contract(abiDefinition)<br>
> byteCode = compiledCode.contracts[':Voting'].bytecode<br>
>deployedContract=VotingContract.new(['Rahul Gandhi','Narendra Modi','Nitish Kumar'],{data:byteCode,from:web3.eth.accounts[0], gas: 4700000})<br>
> deployedContract.address<br>
> contractInstance = VotingContract.at(deployedContract.address)<br>
Step 8 - That’s it! <br>
You can now open the “main.html” file in chrome<br>
It seems like a lot of work, but worth it ;)<br>

![alt text](https://github.com/warmachine0609/Decentralized-Voting-Machine/blob/master/Screenshot.png)


