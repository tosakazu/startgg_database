## Directory Structure

```
data
|_players.json
|_tournaments.csv
|_event2path.csv
|_events
  |_id2path.csv
  |_yyyy
    |_mm
      |_dd
        |_Region
          |_Tounament Name
            |_Event Name
              |_attr.json
              |_matches.json
              |_standings.json
              |_seeds.json
```

## File Schema

### tournaments.csv

```
tournament_id1 tournament_name
tournament_id2 tournament_name
...
```

### event2path.csv

```
event_id1 date2 path1
event_id2 date2 path2
....
```


### players.json

- data: list

  {
  - version: str
  - player_id: str
  - data
    - name: str
    - team: str
    - x_id: str

  }

### attr.json

```
- version: str
- event_id: str
- tounament_name: str
- event_name: str
- date: str
- region: str
- num_entrants: int
- offline: bool
- rule: str
```

#### rule

- gati_1on1
- squad_strike
- oma1
- oma5
- other
- unkown

The rule is estimated by chatgpt with startgg event description.

### matches.json

- version: str
- data: list

  {
  - winner_id: str
  - loser_id: str
  - winner_score: int
  - loser_score: int
  - round: str
  - pool: str
  - dq: bool
  - cancel: bool
  - chara_list: str
  }

### standings.json

- version: str
- data: list of str
  - { player_id1, player_id2, ... }

### seeds.json

- version: str
- data: list of str
  - { player_id1, player_id2, ... }