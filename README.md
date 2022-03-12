# Draft-Craft-Bianance-BSC-
Similar to FIFA Fut Draft, but instead minting TEAM NFTs which are tied to the real world performance of players.


- VRFMintTeam.sol is to be accesed using js frontend.  One can geenrate random players using VRF, then select a subset to be minted and mint the team.
- Payments.sol distributes pot to users who have won..
- UsePayments fills the pot

TODO:
- Make method so that UsePayemts contract can deploy an instance of Payments with pot distributions once winners have been confirmed.
