# Draft-Craft-Bianance-BSC-
Similar to FIFA Fut Draft, but instead minting TEAM NFTs which are tied to the real world performance of players.

Order of Operations for Deployment:
1. In MetaMask, switch to desired blockchain (BSC Mainnet, BSC Testnet, Eth mainnet, Rinkeby)
2. Create a subscription on https://vrf.chain.link/chapel, and record subscription id (id = 188 for current deployment on BSC Testnet).
3. Funcd the subscription with Link Token.
4. In VRFMintTeam.sol, adjust address variables: link, vrfCoordinator and keyHash, to match addresses: Link Token Address, VRF Coordinator address and Key hash, for the chosen network on https://vrf.chain.link/chapel.
5. Deploy VRFMintTeam.sol with id (from step 2) as constructor arg. Record address.
6. Register address (from step 5) on https://vrf.chain.link/chapel/ + id by clicking add consumer and filling in the address.

Fucntionality:
- VRFMintTeam.sol is to be accessed using js frontend.  One can geenrate random players using VRF, then select a subset to be minted and mint the team.
- Payments.sol distributes pot to users who have won.
- UsePayments fills the pot.

TODO:
- Make method so that UsePayemts contract can deploy an instance of Payments with pot distributions once winners have been confirmed.
- https://docs.openzeppelin.com/defender/guide-upgrades
