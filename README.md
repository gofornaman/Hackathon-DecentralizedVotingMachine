This is a submission for the Daksh’18 Hackathon by Guvi.
This project is an amalgamation of two very different modules.
One of the module uses Python exclusively with Flask-API and the other is an ethereum smart contract that runs on Node.js and Soilidity
Please follow these steps religiously
Step 1 - Git clone this rep
Step 2 - Open Command prompt/ Terminal and type in this
		pip install -r requirements.txt
Step 3 - python app.py
Step 4 - Open a new terminal, type in node then npm install ethereumjs-testrpc web3
Step 5 - npm install solc
Step 6 - Go to node_modules/.bin/testrpc and run testrpc
Step 7 - Open a new terminal (again..) and give these commands from node terminal
node
> Web3 = require('web3')
> web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
> web3.eth.accounts
> code = fs.readFileSync('Voting.sol').toString()
> solc = require('solc')
> compiledCode = solc.compile(code)
> abiDefinition = JSON.parse(compiledCode.contracts[':Voting'].interface)
> VotingContract = web3.eth.contract(abiDefinition)
> byteCode = compiledCode.contracts[':Voting'].bytecode
>deployedContract=VotingContract.new(['Rahul Gandhi','Narendra Modi','Nitish Kumar'],{data:byteCode,from:web3.eth.accounts[0], gas: 4700000})
> deployedContract.address
> contractInstance = VotingContract.at(deployedContract.address)
Step 8 - That’s it! 
You can now open the “main.html” file in chrome
It seems like a lot of work, but worth it ;)

![Alt text](Screenshot.jpg?raw=true "This is how it looks")
