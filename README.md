## Imports (web3 & lottery)

Imports web3.js (Ethereum interaction library) and the deployed lottery contract instance.

## Component State (state)

Stores contract details like manager, players, balance, and user inputs (value, message).

## Fetching Contract Data (componentDidMount())

Runs when the component loads.
Fetches manager, players, and contract balance from the blockchain.
Updates the component state.

## Entering the Lottery (onSubmit())

User submits Ether to enter.
Uses web3.eth.getAccounts() to get the user's address.
Calls lottery.methods.enter().send({ from, value }).
Updates the UI with a success message.

## Picking a Winner (onClick())

Calls lottery.methods.pickWinner().send({ from }).
Only the manager can execute this.
Updates the UI with the winner announcement.

## Rendering UI (render())

Displays contract details (manager, players, balance).
Provides form input for users to enter the lottery.
Includes a button for the manager to pick a winner.
Shows real-time transaction messages.
