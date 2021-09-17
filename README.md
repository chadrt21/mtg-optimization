# mtg-optimization
Optimize Magic: The Gathering decks based on theme or card sets

## Architecture (in progess)
### Frontend
Provide selection between preset deck themes or for user to imput select cards to base deck around. 

After processing/optimizing possible deck configurations display deck layout and deck performace metrics (card type distribution, win probability, mana distribution, etc.).
Export functionality (text or pdf) for if the user wants to store results. 
### Backend
#### Getting Data
https://docs.magicthegathering.io/

There are currently ~22,151 non-land MTG cards (Sep 2021). If API call does max 100 cards at a time then it will take ~222 API calls to get all non-land cards (there is a API limit of 5000 requests per hour). *What are the space requirements for all MTG cards?* 

#### Processing/Optimizing
Research Papers:
* [Deckbuilding in Magic: The Gathering Using a Genetic Algorithm](https://ntnuopen.ntnu.no/ntnu-xmlui/bitstream/handle/11250/2462429/16274_FULLTEXT.pdf?sequence=1&isAllowed=y)
* [Monte Carlo search applied to card selection in Magic: The Gathering](https://ieeexplore.ieee.org/abstract/document/5286501)

*What would be O() to simulate n MTG games?*
  * Brute force?
  * Greedy?
  * State Graph?
 
*Which game theory should be implemented in these simulated games?*
