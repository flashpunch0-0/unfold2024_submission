# Blockchain-Powered Federated Learning System

## Project Overview
A comprehensive federated learning system built on blockchain technology, developed for the Unfold Hackathon. This project combines decentralized model parameter storage, secure client-server interactions, and an intuitive user interface to enable distributed machine learning across multiple clients.

## Repository Structure
The project consists of three main components:

### 1. Onchain Model Update API
Backend service managing blockchain interactions and model parameter updates.

### 2. Federated Learning Server-Client
Implementation of the federated learning protocol with server-client architecture.

### 3. BC-FL Landing Page
User interface for monitoring and managing the federated learning system.

## Technical Architecture

### Blockchain Layer (Onchain Model Update API)
- **Smart Contracts**: Ethereum-based parameter storage and verification
- **API Endpoints**: RESTful services for blockchain interactions
- **Queue System**: Bull + Redis for transaction management
- **Tech Stack**:
  - Solidity for smart contracts
  - Node.js & Express.js for API
  - ethers.js for blockchain interaction
  - Winston for logging

### Federated Learning Core (Server-Client)
- **Server Component**: Orchestrates training rounds and model aggregation
- **Client Component**: Handles local training and parameter updates
- **Features**:
  - Secure parameter synchronization
  - Distributed model training
  - Performance metrics tracking

### User Interface (Landing Page)
- **Dashboard**: Real-time training monitoring
- **Analytics**: Model performance visualization
- **Control Panel**: System management interface

## Key Features
- Decentralized model parameter storage
- Secure and transparent training process
- Real-time synchronization across clients
- Comprehensive logging and monitoring
- Scalable architecture supporting multiple clients
- User-friendly interface for system management

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- Redis Server
- Ethereum development environment
- Python 3.8+ (for FL components)

### Installation

1. Clone the repository 

```
git clone https://github.com/your-repo/blockchain-fl.git
```

2. Install APIdependencies

```
cd Onchain_Model_update_API
npm install
```   

3. Setup Federated Learning environment

```
cd ../Federated_Learning_Server_Client
pip install -r requirements.txt
```   

4. Install UI dependencies

```
cd ../BC-FL_Landing_Page
npm install
```   

### Configuration

1. API Configuration (.env)

```
env
RPC_URL=your_ethereum_rpc_url
CONTRACT_ADDRESS=your_contract_address
PRIVATE_KEY=your_private_key
PORT=3000
```

2. FL Server Configuration

``` 
python
Configure server settings in config.py
SERVER_HOST = 'localhost'
SERVER_PORT = 5000
```


3. UI Configuration

```
javascript
// Update API endpoints in config.js
const API_ENDPOINT = 'http://localhost:3000'
```


## Usage

### Starting the System

1. Launch the API Server


```
cd Onchain_Model_update_API
node server.js
```   

2. Start the FL Server

```
cd Federated_Learning_Server_Client
python server.py
```   

3. Run the UI

```
cd BC-FL_Landing_Page
npm start
```   

### API Endpoints

#### Model Parameter Management

```
POST /store-model-parameters
GET /get-model-parameters
GET /get-all-model-parameters
```


#### FL Client Integration

```    
python
from fl_client import FLClient
client = FLClient(client_id=1)
client.connect()
client.start_training()
```



## Security Considerations
- Blockchain-based parameter verification
- Secure client-server communication
- Protected API endpoints
- Data privacy preservation

## Performance Metrics
- Transaction throughput
- Model convergence rates
- System latency
- Training accuracy


## Acknowledgments
- Built for the Unfold Hackathon
- Leverages Ethereum blockchain technology
- Implements federated learning concepts
