# Raffle Smart Contract

## Overview

This project is a decentralized raffle system built on the Ethereum blockchain. It leverages Chainlink's Verifiable Random Function (VRF) to ensure a fair and transparent selection of winners. The raffle allows participants to enter by sending a specified amount of Ether, and after a set interval, a winner is randomly selected to receive the accumulated prize pool.

## Features

- **Decentralized and Transparent**: The raffle is executed on the Ethereum blockchain, ensuring transparency and immutability.
- **Random Winner Selection**: Utilizes Chainlink VRF to provide a provably fair and tamper-proof source of randomness.
- **Automated Upkeep**: The contract automatically checks if the conditions for selecting a winner are met and performs the necessary actions.
- **Configurable Parameters**: The entrance fee, time interval, and other parameters can be configured to suit different use cases.

## Smart Contracts

### Raffle Contract

The core of the project is the `Raffle` contract, which manages the entry of participants and the selection of a winner. Key functionalities include:

- **Enter Raffle**: Participants can enter the raffle by sending the required entrance fee.
- **Check Upkeep**: Determines if the conditions for selecting a winner are met, such as the passage of time and the presence of participants.
- **Perform Upkeep**: Initiates the process of selecting a winner using Chainlink VRF.
- **Fulfill Random Words**: Called by the VRF coordinator to provide the random number used to select the winner.

### Deployment and Interaction Scripts

- **DeployRaffle**: Script to deploy the `Raffle` contract and set up the necessary configurations.
- **Interactions**: Scripts to create and fund VRF subscriptions, and add consumer contracts.

## Testing

The project includes a comprehensive suite of tests to ensure the correct functionality of the raffle system. Tests cover scenarios such as entering the raffle, checking and performing upkeep, and verifying the randomness of winner selection.

## Getting Started

To deploy and interact with the raffle contract, follow these steps:

1. **Install Dependencies**: Ensure you have the necessary tools and libraries installed.
2. **Deploy Contract**: Use the provided deployment script to deploy the `Raffle` contract to your desired network.
3. **Enter Raffle**: Participants can enter the raffle by sending the required Ether to the contract.
4. **Run Tests**: Execute the test suite to verify the functionality of the contract.

