"https://sepolia.scrollscan.dev/address/0xE400BeD016649BE81A844b0FEaFF411176B942c9"

### Sports Betting Platform

This Solidity contract implements a decentralized sports betting platform where users can place bets on different options for an event. The contract supports multiple betting options, event closing, result resolution, and automatic distribution of winnings.

#### Contract Overview

- **Owner:** The owner of the contract can close the event, resolve the event, and set the correct option after event closure.
- **Event State:** The event can be in one of three states: OPEN, CLOSED, or RESOLVED.
- **Betting Options:** Each betting option contains a total bet amount and a mapping of user bets.
- **Events:** The contract emits events for bet placement, event closure, event resolution, withdrawal, and commission withdrawal.
- **Commission Rate:** The commission rate, set by the owner, determines the platform's commission on total bets.
- **Closing Time:** The closing time of the event is set during contract deployment.
- **User Winnings:** Users can withdraw their winnings from the platform.
- **Correct Option Index:** After event closure, the owner sets the correct option index.

#### Functions

- **Constructor:** Initializes contract variables including commission rate, closing time, and betting options.
- **placeBet:** Allows users to place bets on a selected option by sending ether along with the option index.
- **closeEvent:** Allows the owner to close the event when the betting period is over.
- **resolveEvent:** Allows the owner to resolve the event and distribute winnings.
- **setCorrectOption:** Allows the owner to set the correct option index after event closure.
- **distributeWinnings:** Distributes winnings to users who placed bets on the correct option.
- **getUsers:** Returns an array of users who placed bets on a specific option.
- **withdrawWinnings:** Allows users to withdraw their winnings from the platform.
- **cancelBet:** Allows users to cancel their bets before the event closes and receive a refund.

#### Usage

1. Deploy the contract, specifying the commission rate, closing time, and betting options.
2. Users can place bets on selected options by calling the `placeBet` function with the chosen option index and sending ether along with the transaction.
3. After the betting period ends, the owner can close the event and set the correct option index.
4. The owner can then resolve the event, and winnings will be automatically distributed to users who placed bets on the correct option.
5. Users can withdraw their winnings using the `withdrawWinnings` function.

#### Verification

The code has been verified on Sepolia Scan. You can view the verification page [here](https://sepolia.scrollscan.dev/address/0xE400BeD016649BE81A844b0FEaFF411176B942c9).
