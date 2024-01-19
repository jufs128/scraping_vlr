The notebook in this repository scrapes data from vlr.gg, creating three different .csv files with info from matches, maps and players. Each file contains the following columns:

**• matches.csv (match_info_df):**
  - Match_URL: completing URL for the match (paste after 'vlr.gg')
  - Tournament: name of the tournament the match happenned in
  - Team_1: first team who played the match
  - Score_1: number of maps won by the first team
  - Team_2: second team who played the match
  - Score_2: number of maps won by the second team

**• maps.csv (map_info_df):**
  - Match_URL: completing URL for the match in which the map was played (paste after 'vlr.gg') 
  - Map_Name: name of the map (ex.: Ascent, Breeze...)
  - Map_ID: identifier for this specific match on the map
  - Duration: how long the map was played for
  - Team_1: first team who played the map
  - URL_1: completing URL for the first team (paste after 'vlr.gg')
  - Start_Side_1: starting side of the first deam (T or CT)
  - Score_1: number of rounds won by the first team
  - Attacking_Score_1: number of rounds won by the first team on attack
  - Defending_Score_1: number of rounds won by the first team on defense
  - Team_2: second team who played the map
  - URL_2: completing URL for the second team (paste after 'vlr.gg')
  - Start_Side_2: starting side of the second deam (T or CT)
  - Score_2: number of rounds won by the second team
  - Attacking_Score_2: number of rounds won by the second team on attack
  - Defending_Score_2: number of rounds won by the second team on defense

**• players.csv (player_info_df):**
  - Match_URL: completing URL for the match this stats refer to (paste after 'vlr.gg')
  - Map_ID: identifier for the map this stats refer to
  - Team_URL: completing URL for the player's team (paste after 'vlr.gg')
  - Player_Name: nickname of the player
  - Player_URL: completing URL for the player (paste after 'vlr.gg')
  - Agents: agent
  - Rating Attacking: player's rating on attack
  - Rating Defending: player's rating on defense
  - Rating: player's general rating
  - ACS Attacking: player's ACS on attack
  - ACS Defending: player's ACS on defense
  - ACS: player's general ACS
  - K Attacking: player's kills on attack
  - K Defending: player's kills on defense
  - K: player's general kills
  - D Attacking: player's deaths on attack
  - D Defending: player's deaths on defense
  - D: player's general deaths
  - A Attacking: player's assists on attack
  - A Defending: player's assists on defense
  - A: player's general assists
  - +/- Attacking: player's kills minus deaths on attack
  - +/- Defending: player's kills minus deaths on defense
  - +/-: player's general kills minus deaths
  - KAST Attacking: player's KAST on attack
  - KAST Defending: player's KAST on defense
  - KAST: player's general KAST
  - ADR Attacking: player's ADR on attack
  - ADR Defending: player's ADR on defense
  - ADR: player's general ADR
  - HS Attacking: player's headshot % on attack
  - HS Defending: player's headshot % on defense
  - HS: player's general headshot %
  - FK Attacking: player's first kills on attack
  - FK Defending: player's first kills on defense
  - FK: player's general first kills
  - FD Attacking: player's first deaths on attack
  - FD Defending: player's first deaths on defense
  - FD: player's general first deaths
  - FK_FD_+/-: player's first kills minus first deaths rating
  - Attacking FK_FD_+/-: player's first kills minus first deaths on attack
  - Defending FK_FD_+/-: player's first kills minus first deaths on defense
  - 2K: number of player's 2 kills in one round
  - 3K: number of player's 3 kills in one round
  - 4K: number of player's 4 kills in one round
  - 5K: number of player's 5 kills (ace) in one round
  - 1v1: number of player's wins on 1 vs 1
  - 1v2: number of player's wins on 1 vs 2
  - 1v3: number of player's wins on 1 vs 3
  - 1v4: number of player's wins on 1 vs 4
  - 1v5: number of player's wins on 1 vs 5
  - ECON: player's economy rating
  - PL: number of times player planted
  - DE: number of times player defused


**Parameters to alter:**
- You can alter the number of pages the algorithm will go through and the starting page when calling the function _get_stats()_ on cell number 8.
- This code currently filters for tournaments with "Challengers" or "Champions" included in the name, this can also be altered on cell number 8, inside the function _get_stats()_.
