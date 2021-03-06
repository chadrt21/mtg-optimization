# mtg-optimization
Optimize Magic: The Gathering decks based on theme or card sets

## Architecture (in progess)
### Frontend
User selection:
 * Preset deck colors/themes (mono red, Izzet, Angels, etc.) or select cards to base deck around
 * Game Legality (Modern, Historic, Commander, etc.)  

After processing/optimizing possible deck configurations display most optimial deck layout and deck performace metrics (card type distribution, win probability, mana distribution, etc.).
Have export functionality (text or pdf) for if the user wants to store results. 
### Backend
#### Getting Data
https://docs.magicthegathering.io/

There are currently ~22,151 non-land MTG cards (Sep 2021). If API call does max 100 cards at a time then it will take ~222 API calls to get all non-land cards (there is a API limit of 5000 requests per hour). *What are the space requirements for all MTG cards (in JSON like format)?* 

#### Processing/Optimizing
Research Papers:
* [Deckbuilding in Magic: The Gathering Using a Genetic Algorithm](https://ntnuopen.ntnu.no/ntnu-xmlui/bitstream/handle/11250/2462429/16274_FULLTEXT.pdf?sequence=1&isAllowed=y)
* [Monte Carlo search applied to card selection in Magic: The Gathering](https://ieeexplore.ieee.org/abstract/document/5286501)

##### Deck Building
If there are 60 cards in a deck and 17-36 lands per deck (depending on mana curve), then there could be anywhere from 1.12e134 to 3.09e80 possible cards choices per deck. This can be reduced by restrictions such as card themes (Angles, Merfolk, etc.) or colors (Blue, Red, etc.). 

Instead of trying to generate a whole new deck each time, generate a deck from a deck seed (preset deck sub-set). 

Common MTG deck archetypes:
* Aggro
* Control
* Combo
* Midrange

##### Deck Testing
Would machine learning/AI be required to test decks? Or could it be statistically analyzed by some meteric(s) that could indicate probability of winning? 

*What would be O() to simulate n MTG games?*
  * Brute force?
  * Greedy?
  * State Graph?
 
*Which game theory should be implemented in these simulated games?*
 * *How do you choose which cards to play?*
 * *WHen to use a instant spell?*
