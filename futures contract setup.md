# Futures contracts setup

Futures contracts setup window allows to add/edit/remove futures contracts (commodities, equties, fx, bond and rates). Futures contracts are being created and expired periodically. We wanted to automate generating new futures contracts that traders are actively trading.
- Administrator from Back Office will add new ticker, bloomber yellowkey, months that contracts are available and how far the contracts should be created each month.
- Futures contracts setup detail will be stored in the database.
- At first day of each month, a schedule job will be run and put together new futures contract symbols like 'CLF24 Comdty' 
- This contract symbol will be passed to the Bloomberg API to download the valid futures contract detail.
- Then the process calls the internal API to insert the futures contract info into the Security Master.

![Alt text](assets/futures%20contract%20entry.png)