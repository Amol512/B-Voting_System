## Decentralized Voting (B-Voting System)

A decentralized voting system based on [Ethereum blockchain](https://ethereum.org/dapps/) technology.

## Report
https://github.com/Amol512/B-Voting_System/blob/master/Report.pdf


### Dependencies

- [Node.js](https://nodejs.org)
- [Truffle](https://www.trufflesuite.com/truffle)
- [Ganache](https://trufflesuite.com/ganache/)
- [Metamask](https://metamask.io/) (Browser Extension)

#### nodejs and npm
  
```shell
$ sudo apt install nodejs
$ sudo apt install npm
```
  In case of error while installation [Click Here](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04)

#### Truffle
```shell
$ sudo npm install -g truffle
```

#### Download and run Ganache
  Download Ganache
  https://trufflesuite.com/ganache/

  open terminal where ganache is dowloaded.
``` 
$ chmod +x ganache-2.5.4-linux-x86_64.AppImage
$ ./ganache-2.5.4-linux-x86_64.AppImage
```
#### Metamask
https://www.geeksforgeeks.org/how-to-install-and-use-metamask-on-google-chrome/
#### Step 1. Clone repository
```
 $ git clone https://github.com/Amol512/B-Voting_System.git
```
#### Step 2. Start Ganache
Open the Ganache GUI client that you downloaded and installed. This will start your local blockchain instance.
```
 $ ./ganache-2.5.4-linux-x86_64.AppImage
```
#### Step 3. Configure Metamask
https://www.geeksforgeeks.org/how-to-set-up-ganche-with-metamask/
- Unlock Metamask
- Connect metamask to your local Etherum blockchain provided by Ganache.
- Import an account provided by Ganache
- New RPC URL: http://localhost:8545
- Chain ID: 1337

#### Step 4. Compile & Deploy Election Smart Contract
```
 $ truffle migrate --reset
```
You must migrate the election smart contract each time your before starting server.

#### Step 5. Launch server (frontend)
```
 $ cd client
 $ npm install
 $ npm start
```
Visit this URL in your browser: http://localhost:3000

### System Workflow
A brief explanation on the basic workflow of the application.

- Admin will create a voting instance by launching/deploying the system in a blockchain network, then create an election instance and start the
  election with the details of the election filled in (including candidates for voters to vote).
- Then the likely voters connect to the same blockchain network register to become a voter. Once the users successfully register, their respective 
  details are sent/displayed in the admins' panel (i.e. verification page).
- The admin then will check if the registration information (blockchain account address, name, and phone number) is valid and matches with his record. If 
  yes, then the admin approves the registered user making them eligible to take part and cast their respective vote in the election.
- The registered user (voter) following the approval from the admin casts their vote to the candidate of interest (from the voting page).
- After some time, the admin ends the election. As that happens the voting is closed and the results are displayed 
  announcing the winner at the top of the results page.
  
## Admin 
 - Add Candidate for Election.
 - can Start and End Election.
 - Verification of Registered voter's has to done by Admin. unless voter can't able to make vote.
 - Admin can also Registered itself for voting.
 - After Registration of admin itself he can able to vote for election.
 - Admin have to End Election, for Results.

## Voter
 - Voter has to registered himself/herself for voting and wait for Admin Approval/verification.
 - if admin approve/verify voter then and then only voter can vote in ongoing election.
 - when admin ends ongoing election then voters can see results.

## Note
To login in a system you need to import accounts from ganache.
each voter requied different metamask account also admin has there own different metamask account (which is by default index 0 account from ganache).
Select account in metamask extention and just refresh the page account detail will be get available.
If you performed any operation and things will not get reflected then please refresh the page.

## GUI
### Admin View
![Admin](https://github.com/Amol512/B-Voting_System/blob/master/Screenshots/Admin.png)
### Voter View
![Voter](https://github.com/Amol512/B-Voting_System/blob/master/Screenshots/Voter_View.png)
### Metamask
![Metamask](https://github.com/Amol512/B-Voting_System/blob/master/Screenshots/Metamask.png)


#### More
 -to unbox truffle box use
 ```
  $ truffle unbox react
```

#### Icons
far fa-registered : 
https://fontawesome.com/v4/icon/registered

fas fa-vote-yea :
https://fontawesome.com/v5/icons/vote-yea?style=light&s=solid

fas fa-poll-h :
https://fontawesome.com/v5/icons/poll-h?style=solid&s=solid

Explore more icons on :
https://fontawesome.com/



