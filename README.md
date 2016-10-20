# Usage

Contents of this directory should be copied to ~/bin/

- `fake-urbit ship [ship]` will start each **ship** in the current directory, creating them and all parents if necessary. For non-galaxies, at least one ship must already be running to bootstrap `(sein)` calculation.
- `children n ship [ship]` will ask each **ship** for the names of their firs **n** children
- `federate channelname ship [ship]` will clear current `%channelname` subscriptions on each **ship**, then link them in a fully connected graph
- `join channel ship [ship]` will subscribe each **ship** to `/channel`

# Dependencies

- urbit compiled @ piers-json (TODO: merge)
- urb.py (should use piers.json)
- arvo @ automount
- screen

# Todo

## Variables

- `URBIT` bin/urbit location
- `SCREEN` to determine which screen session to run new urbits in, leave blank for direct start in same process (daemon mode maybe?)
- `FAKE`, start on real net if absent

## Scripts
- make-vere, make-pill at a commit
- provision gcloud instances