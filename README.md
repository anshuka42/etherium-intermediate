# Etherium intermediate project-Let's vote..
Etherium intermediate project having a contract simple voting which show a basic voting system with the idea of let's vote.
## Description
Here we have a contract simple voting which show a basic voting system that demonstrates different ways to handle errors and validate conditions in Ethereum smart contracts. It includes examples of using require, revert, and assert statements.
## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., etherium_project.sol). 
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy" tab in the left-hand sidebar and giving the list of all participating candidates in the form of array.
## Vote Function
This function allows an address to vote for a candidate.
The function checks if the provided candidate is valid by comparing the candidate's name against the list of candidates 
The function emits a VoteCast event.
## EndVoting Function
This function ends the voting process.Ensures that only the contract owner can end the voting.
If voting is already ended, the function will revert.
The function emits a VotingEnded event.
## TotalVotesFor Function
This is a view function that returns the total number of votes a specific candidate has received. It does not modify the state, so it is marked as view.
## GetCandidates Function
This is a view function that returns the list of candidates.
## Use of error handler
require(votingActive) Ensures that voting is still active. If voting has ended, the function will revert.
require(!hasVoted) Ensures that the voter has not already voted.
assert(hasVoted) This statement is an additional check to ensure that the vote was recorded successfully.
revert If voting is already ended, the function will revert.
## Authors
Anshuka
github profile link:-https://github.com/anshuka42
## License
This project is licensed under the MIT License - see the Create LICENSE file for details
