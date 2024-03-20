# 3040Crypto Wallet API

## API Description

The 3040Crypto Wallet API enables users to interact with their cryptocurrency wallets, allowing them to view balances, access transaction histories, and initiate transfers. This API is designed for seamless integration with the 3040Crypto ecosystem to manage digital assets efficiently.

## Endpoints and Parameters

### Get Wallet Balance

- **Endpoint:** `/wallet/balance`
- **Method:** `GET`
- **Parameters:**
  - `walletId`: Unique identifier for the user's wallet.
- **Description:** Retrieves the current balance of the specified wallet in various cryptocurrencies.

### Get Transaction History

- **Endpoint:** `/wallet/transactions`
- **Method:** `GET`
- **Parameters:**
  - `walletId`: Unique identifier for the user's wallet.
  - `limit`: Optional parameter to limit the number of returned transactions.
- **Description:** Returns a list of recent transactions for the specified wallet.

### Initiate Transfer

- *Endpoint:* /wallet/transfer
- *Method:* POST
- *Parameters:* (in the request body)
  - fromWalletId: Sender's wallet identifier.
  - toWalletId: Recipient's wallet identifier.
  - amount: Amount of cryptocurrency to transfer.
  - currency: Type of cryptocurrency to transfer.
- *Description:* Executes a transfer of a specified amount of cryptocurrency from one wallet to another.

## Description of Resources

json

{
  
  "Wallet": {
  
    "walletId": "string",
    
    "balance": {
    
      "BTC": "number",
      
      "ETH": "number",
      
      "LTC": "number"
    
    },
    
    
    "transactions": [
    
    {
    
        "transactionId": "string",
        
        "amount": "number",
        
        "currency": "string",
        
        "timestamp": "datetime",
        
        "type": "string"
      
      }
      
    ]
  
  }

}

