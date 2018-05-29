# SGChain api

On this page:

* [API](#api)

## API

### /POST
### Wallet
#### /getetherbalance
Returns your ether balance
##### Request
```
curl 
     --header "Content-Type: application/json" 
     --request POST  --data "{"account": "ACCOUNT_TO_CHECK"}"
   http://localhost:9001/getetherbalance
```
##### Response
```
{
  "balance": "YOUR_ETHER_BALANCE"
}
```
- - -
#### /getbalance
Returns your SGCC balance
##### Request
```
curl
     --header "Content-Type: application/json" 
	 --request POST --data '{"account":"YOUR_ACCOUNT_ADDRESS", "password":"YOUR_PASSWORD"}' 
   http://localhost:9001/getbalance
```
##### Response
```
{
  "balance": "YOUR_SGCC_BALANCE"
}
```
- - -
#### /transfertoken
Transfer SGCC token to another account
##### Request
```
curl 
     --header "Content-Type: application/json" 
     --request POST  --data "{"youraccount": "YOUR_ACCOUNT_ADDERSS", "password": "YOUR_PASSWORD",
	 "toaddress": "ACCOUNT_ADDRESS",    "amount": "AMOUNT_TO_SEND",
	 "gaslimit":"GAS_LIMIT", "gasprice":"GAS_PRICE_IN_GWEI"}"
   http://localhost:9001/transfertoken
```
##### Response
```
{
  "transactionhash": "0xTRANSACTIONHASH"
}
```
- - -
#### /createwallet
coming soon!
- - -
#### /register
coming soon!

## Setup
To run the example, you'll need node.js.
Simply run the ethererum node on the side, then start the server.