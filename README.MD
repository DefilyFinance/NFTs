### Deployment:
 - Install `truffle` as global scope
 - Run flatten to flatten needed contracts
 - Use Remix to deploy contracts:
    + First,...

### Test:
 - Similar process to deployment, with minor changes:
    + Deploy ...
  
### Generic flow:
  1. owner can `whitelist` an admin for minting and recovering NFTs. Owner can also `dewhitelist` an admin in case of emergency
  2. admin `mint` an NFT with its `nftInfo` (fee, unlockedTime, expiredTime) which will be owned by the ASSXNFT contract (in case admin lost the account or multiple admins)
  3. user `claim` an NFT which will pay the fee (excess amount will be returned to user) and get the NFT:
    a. when the NFT is locked, user can not transfer, transferFrom, approve the NFT by any means until it is unlocked
    b. when the NFT is expired, user can not transfer, transferFrom, approve the NFT by any means. An expired NFT can be `recover` by the admin(s)
  4. admin will recover and NFT that has expired, which will also delete the `nftInfo` of that NFT and send that back to the ASSXNFT contract (will be the storage contract/wallet in the future)
  

### Settings:
- constructor:
    + ...

### Roles:
  1. ...

...

### Variables:
  1. ...

### Functions:
- MAIN:
   1. 

- SUPPORTING:
    1. ....

- SETTERS:
    1. ...

- GETTERS:
    1. ...

