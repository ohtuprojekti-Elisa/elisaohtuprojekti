
### provider

- Information about the game provider.
    - **`name`**: Name of the game (`string`).
    - **`appid`**: Application ID (`integer`).
    - **`version`**: Game version (`integer`).
    - **`steamid`**: Steam ID of the player (`string`).
    - **`timestamp`**: Timestamp of the data (`integer`).

---
### map

- Information about the game map and match.
    - **`mode`**: Game mode (`string`).
    - **`name`**: Map name (`string`).
    - **`phase`**: Match phase (`string`).
    - **`round`**: Current round number (`integer`).
    - **`team_ct`**: Counter Terrorist -team statistics.
        - **`score`**: CT score (`integer`).
        - **`consecutive_round_losses`**: Consecutive losses (`integer`).
        - **`timeouts_remaining`**: Timeouts left (`integer`).
        - **`matches_won_this_series`**: Matches won in the series (`integer`).
    - **`team_t`**: Terrorist-team statistics.
	    - **`score`**: T score (`integer`).
        - **`consecutive_round_losses`**: Consecutive losses (`integer`).
        - **`timeouts_remaining`**: Timeouts left (`integer`).
        - **`matches_won_this_series`**: Matches won in the series (`integer`).
    - **`num_matches_to_win_series`**: Number of matches needed to win the series (`integer`).
    - **`round_wins`**: Dictionary mapping round numbers to outcomes (`dictionary` of `string`).
    - current_spectators ?
    - souvenirs_total ?

---
### round

- Information about the current round.
    - **`phase`**: Phase of the round (`string`).

---
### player

- Information about the active player.
    - **`spectarget`**: Target being spectated (`string`).
    - **`position`**: Player's position in the map (`string`).
    - **`forward`**: Forward direction vector (`string`).
    - steamid ?
    - name ?
    - activity ?
    - observer_slot ?

---
### phase_countdowns

- Phase countdown information.
    - **`phase`**: Current phase (`string`).
    - **`phase_ends_in`**: Time left in the current phase (`string`).

---
### allplayers

- Information about all players.
    - **Keys**: Steam IDs (`string`).
    - **Values**:
        - **`name`**: Player's name (`string`).
        - **`observer_slot`**: Observer slot number (`integer`).
        - **`team`**: Team affiliation (`string`, either "T" or "CT").
        - **`state`**: Player state.
            - **`health`**: Health level (`integer`).
            - **`armor`**: Armor level (`integer`).
            - **`helmet`**: Whether wearing a helmet (`boolean`).
            - **`flashed`**: Flashbang effect intensity (`integer`).
            - **`smoked`**: Smoked status (`integer`).
            - **`burning`**: Burning status (`integer`).
            - **`money`**: Money available (`integer`).
            - **`round_kills`**: Kills in the current round (`integer`).
            - **`round_killhs`**: Headshot kills in the round (`integer`).
            - **`round_totaldmg`**: Total damage in the round (`integer`).
            - **`equip_value`**: Equipment value (`integer`).
        - **`match_stats`**:
            - **`kills`**: Total kills (`integer`).
            - **`assists`**: Total assists (`integer`).
            - **`deaths`**: Total deaths (`integer`).
            - **`mvps`**: MVP awards (`integer`).
            - **`score`**: Player score (`integer`).
        - **`weapons`**: Dictionary of equipped weapons.
            - **Keys**: Weapon IDs (`string`, e.g., `weapon_0`).
            - **Values**:
                - **`name`**: Weapon name (`string`).
                - **`paintkit`**: Paintkit/skin (`string`).
                - **`type`**: Weapon type (`string`).
                - **`ammo_clip`**: Ammo in the clip (`integer`, optional).
                - **`ammo_clip_max`**: Maximum clip size (`integer`, optional).
                - **`ammo_reserve`**: Ammo in reserve (`integer`, optional).
                - **`state`**: Weapon state (`string`, e.g., `holstered`, `active`).
        - **`position`**: Player position (`string`).
        - **`forward`**: Forward direction vector (`string`).
        - activity ?
        - HasDefuseKit

