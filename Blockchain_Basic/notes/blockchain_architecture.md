### Blockchain Architecture Overview

- Consesus problem - come to an an aggreement
- Sybil attacks - many nodes weight or creating psedoanonymous account on to the blockchain
- Sybill Ressistance Mechanism(Pows and Pos )-> stake ETH meight be slashed if the nodes mis behave
- Finality - the txn confirmed by the node can not be reverted unlike bank txn
- After 6 blocks confirm added the probability of reversing it is minimum
- Rewriting all the transaction history consume to much power

### What is Hash and SHA256 algorithm?

- A unique fixed length of string used to identify a piece if data
- Block , nonce , Data and finally Hash for the inserted data
- Bruteforce - miners trying to solve the the nonce number which give the hash number starting with four zeros at the beggining of the hash.
- Genesis block - the first block in the blockchain , mostly it has all the zeros in the hash number .
- Fork - blockchain splits - longest chain rule
- Meme pool - is place where all the transaction lives there before added to the blockchain
- Signature - signing txn with a key
- Cryptographic key -
- Private key - we use to sign txn , like signature stamp
- Public key - its like email address - can verify signature created by our private key and they are linked by math, one way
- our wallet address is linked to our public key or its in short hashed version of it
- in metamask confirm means we are creating digital signature using our private key
- https://demos.updraft.cyfrin.io/ecdsa - use this demo to practice - its all inclusive
- Pows => Miners
  -Pos => Validator stake eth
- Keccak256 Hashing - algo - they are determistic , unique - > one way function

### How Block Hashing Works:

• Block Components: All block data (block number and associated data) is combined

• Deterministic Process: Same block data always produces the same hash

• Avalanche Effect: Changing any data completely changes the hash

• Fixed Output: Hash is always 256 bits (64 hex characters) regardless of input size

• Unique Fingerprint: Each unique block gets a unique hash - no two different blocks can have the same hash

• Next Step: Once hashed, this unique fingerprint can be cryptographically signed by the block proposer

### How Block Signing Works:

• Hash Calculation: Block hash is calculated from all block components (number, previous hash, data, validator, timestamp)

• Signing Process: The validator cryptographically signs the calculated hash

• Verification: Any change to block data changes the hash, invalidating the signature

• Security: This prevents tampering - any modification is immediately detectable

• Ethereum Reality: Real validators sign block hashes using their private keys

![alt text](image-1.png)

### Pos Blockchain

- Any one can become a validator after staking ETH and participating on the network need to have at least 32 ETH and max is 2048 ETH.

- ![alt text](image-2.png)
- Then validators need to validate based on the proposal
- ![alt text](image-3.png)
- After all they vote on the proposal and it will go to finality stage. if total 2/3 vote yes then it go to final stage and becomes irrivesable.
- Majority rules!

- POS dont have nounce instead they have signing .

- Validators randomly chosen (Pseudo Rando) algorithm 

### Slashing

- If the validators mis consduct and violate consus they will be punished , slashed their portion of stake is called burning (Taken out of circulation) or destroying.

- Validators can vote for punishment -   incase double signing blocks  , going offline mostly , surround voting - . other can prof this using cryptography for this violation to trigger the slashing mecahnism.

- Every 12 sec(this is called Slots) the validator propose its block  and other committe just vote to validate all nned to aggree.
- 32 Slots called Epoch = 6.4 minute or (its means that 12 * 32 /60) 
- justified block  is the next  block immidiately after the finalized block and  then it will be -> final block (finality).
- Game theory - an economic insentive to secure the network  while contributing to the network (cheaper than attack) and more benefial than attacking the network.(economic incentive)

### You can become a validator as well

- ![alt text](image-4.png)
