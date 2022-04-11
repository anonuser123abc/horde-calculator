# How to use horde calculator

 - **[ Version 2 ](#version-2)**<br>
 - **[ Version 1 ](#version-1)**<br>


## Version 2
Link: https://anonuser123abc.github.io/horde-calculator/v2/

This version has many new features, and it also contains the old version in the tab "Simple Calculator"

#### Templates
Here you can create templates which are like detailed plans of plots and NFTs. You can create, edit, copy and delete templates! The templates are persisted on your device local storage, so if you use same browser on the same device, you will have your templates whenever you open the calculator.

There is a special template (which will be visible when calculator v2 is loaded from dApp in future), this special template is called "Live Wallet" and represents your current wallet, you can not delete this template as it doesnt actually exist, its only your current wallet state. But you can edit it and copy it.

When creating or editing template you can create plot groups, which consist of date of creation (and decay) and how many plots were created that day. 

You can also add 5%/10%/15% NFTs, as many as you like.

#### Calculator
Some fields as in the old version but most are new.

1. "Template" - choose a template which you want to simulate (similar to "How many plots" in the old version)
2. "Claimable tokens" - how many reward tokens you have claimable at the moment, if you didn't yet start with the investment just put 0 
3. "Duration in future" - how many days in future to run the simulation
4. "# Wallets Hardcap" - you can have max 100 plots per wallet. This is a hard limit in the HORDE protocol, it serves as discouragement for exponential compounding. Therefore you can choose how many wallets would you use - min 1, max 5
5. "$$$ Invested (optional)" - here you can put how much you have invested which is necessary for the Cashout Until Breakeven strategy
6. "$$$ Cashed Out Already (optional)" - same as Invested field

There are 2 calculator strategies for now.
First one is full compound (identical to simple calculator). Second strategy is first cashing out your investments, and only then full compound. More strategies could be added in the future.


When compounding, calculator will continue to compound until the wallet limit is hit, then it will cashout and just maintain active plot count at the limit.

##### Graphs
There are 3 graphs with different information. Each dataset can be hidden/shown by clicking on its label.

1. Plot Graph - this graph shows count of active and decayed plots though time
2. Cashout graph - this graph is about money, it shows total cashout profit and tax (if 10 tokens are sold, 9 go into cashout profit, 1 goes to sell tax), daily cashout profit and tax, if the "Invested" input is populated it will also show a break-even line
3. Two tokenomics graphs, one in HORDE, one in $$$, basically just shows how creating plots feeds the ecosystem

##### Details about calculator
 - calculator creates new plots at the beginning of a day if it has enough rewards
 - on the last day, plot will generate the reward and then move into 'decayed' status
 - nfts:
   - one plot can only have one NFT, and one NFT can only be assigned to one plot, its 1 to 1 relationship
   - considering that, if you have more plots than NFTs, calculator will assume all NFTs have been assigned and are active
   - BUT if you have more NFTs than you have plots, then calculator will assume that the highest reward NFTs are assigned first

## Version 1
Link: https://anonuser123abc.github.io/horde-calculator/v1/

Currently used by dApp

The old version is simple to use but lacks in features, however it is still very useful if you are NEW to the project. This calculator assumes plots were created today, and will simply compound (at the end of the day) whenever there are enough rewards.

It offers three inputs:
1. "How many plots" - how many plots you have or how many plots do you want to start with
2. "How many claimable tokens" - if you have already started and have some rewards that are claimable, put them here
3. "Duration in future" - how many days in future to run the simulation

Note - in horde ecosystem you can have max 100 plots per wallet, but this simple old version is not taking that into account, so it will compound like crazy without any limits

