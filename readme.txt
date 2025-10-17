# CPSC 559 - Advance Blockchain Technologies

## Mid Term Project

## Team members: My Zombie DApp Team

1. Hardavi Thoria : 829265453 (hardavit@csu.fullerton.edu)
2. Pranav Sheth :  810028118 (PranavSheth@csu.fullerton.edu)

## Professor

Prof. Wenlin Han, CSU Fullerton: whan@fullerton.edu

## Project Overview

This is a decentralized application built on blockchain technology that enables users to interact with smart contracts to generate, customize, and enhance their own zombie characters. Our implementation includes an intuitive web interface that connects directly with MetaMask for secure wallet transactions.

## Key Features

1. **Zombie Generation** - Users can create unique zombie characters with personalized names
   - **Batch Creation:** Input multiple names separated by commas for bulk creation
   - Example input: "Zombie1, Zombie2, Zombie3" creates three zombies simultaneously
2. **Character Progression** - Pay transaction fees to increase your zombie's level
3. **Collection Display** - Browse and view detailed information about all zombies in your wallet
4. **Audio Controls** - Toggle button for background soundtrack playback

## Enhancements Beyond Base Project

1. Designed the user interface with modern styling and animations
2. Implemented dynamic zombie naming system (user-defined names)
3. Developed batch zombie creation functionality
4. Added name-based zombie selection for leveling up
5. Removed hardcoded values to make the application fully dynamic
6. Integrated audio player with toggle controls

## Interface Design Improvements

1. **Visual Styling:**
   - Applied gradient color schemes to action buttons (purple, pink, and cyan)
   - Each button has distinct visual identity matching its function
   - Interactive elements respond to user hover with smooth transitions

2. **Layout Architecture:**
   - Buttons arranged in triangular pattern for visual appeal
   - Primary action (creation) positioned centrally at top
   - Secondary actions (view/upgrade) aligned horizontally below

3. **Animation & Effects:**
   - Title features luminous green border with glow effect
   - Button interactions include elevation animation on hover
   - Character cards display dynamic hover states with border illumination
   - Optimized background opacity for improved content readability

4. **Personalization:**
   - Custom application title: "My Zombie DApp"
   - Unique zombie character artwork as background (SCR-20251016-ktfs.png)
   - Custom background music (audio/AUDIO.mp3) with toggle controls
   - Thematic typography with Press Gothic font

5. **User Experience Optimizations:**
   - Automatic blockchain network detection and switching (Chain ID: 1337)
   - Icon-enhanced button labels for improved comprehension
   - Real-time transaction status updates with visual feedback
   - Mobile-friendly responsive layout

6. **Advanced Batch Processing:**
   - Multi-character creation in single transaction sequence
   - Comma-delimited name parsing functionality
   - Live progress indicator during batch operations
   - User confirmation prompt before executing bulk actions
   - Graceful error recovery for failed individual transactions 

## Technology Stack

- **Smart Contracts:** Solidity 0.8.11
- **Development Framework:** Truffle v5.4.25
- **Local Blockchain:** Ganache v2.5.4
- **Web3 Integration:** Web3.js v1.2.7
- **Frontend:** HTML5, CSS3, JavaScript, jQuery
- **Wallet:** MetaMask
- **Node.js:** v14.16.0


# Setup Guide


## Prerequisites and Installation:
- Download and install MetaMask browser extension from the Chrome Web Store
- Install Ganache for local blockchain simulation
- Verify your development environment includes these specific versions:
     Truffle v5.4.25
     Ganache v2.5.4
     Solidity - 0.8.11 (solc-js) 
     Node v14.16.0
     Web3.js v1.2.7

## Step 1: Initialize Local Blockchain
- Launch Ganache in Quickstart mode
- Navigate to Settings and link your Truffle configuration file (truffle_config.js)

## Step 2: Compile and Deploy Smart Contracts
Open terminal in your project directory and run:
```
truffle compile
truffle migrate
```
Ensure your Truffle configuration matches Ganache's localhost settings.

## Step 3: Update Contract Address
- After successful migration, copy the deployed contract address
- Replace the contract address in index.html with your newly deployed address

## Step 4: Configure MetaMask Network
Add a custom network in MetaMask with these parameters:
- Network Name: Localhost
- RPC URL: http://127.0.0.1:7545
- Chain ID: 1337
- Currency Symbol: ETH

Verify that Ganache is using the same RPC server configuration.

## Step 5: Import Development Account
- Copy a private key from one of Ganache's test accounts
- Import this private key into MetaMask
- Switch MetaMask to the Localhost network

## Step 6: Launch Application
Start the web server with this command:
```
npx http-server -p 3000
```
Access the application at: http://localhost:3000

## Step 7: Connect Wallet
- Navigate to http://localhost:3000 in your browser
- Connect your MetaMask wallet when prompted

## Step 8: Testing
Explore all features: create zombies, view your collection, and level up characters!