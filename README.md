# Install

- clone with `--recursive`, or run `git submodule update --init`
- install `python`, `jq`, and the `urbit` dependencies
- `make -C urbit/`
- (optionally) add `$(pwd)/bin/` to `PATH`

# Usage

Piers are created in the calling directory, and subsequently restarted from the same.

- `make-urbit ship` will produce the `urbit` arguments to create/restart the **ship**
- `fake-urbit ship [ship]` will start a local fakenet
- `start-urbit ship [ship]` will start each **ship** in the current directory, creating them and all parents if necessary. For non-galaxies, at least one ship must already be running to bootstrap `(sein)` calculation.
- `start-urbit-on instances ship [ship]` will start each **ship** on a randomly chosen instance
- `children n ship [ship]` will ask each **ship** for the names of their firs **n** children
- `federate channelname ship [ship]` will clear current `%channelname` subscriptions on each **ship**, then link them in a fully connected graph
- `join channel ship [ship]` will subscribe each **ship** to `/channel`

- `some of them` NOTE: `screen` must be installed

## Variables

- `FAKE`, set this to use `-F` local fakenet

# Submodules

This repository includes:

- arvo @
  + automount, mounting %home on startup
  + 0w0-imperator which harcodes the expected carrier `-G` to `0w0`
- urbit @
  + ports-json, which writes .urb/ports.json
  + testzod-urbit-org, which sets the `%ames` bootstrapping dns to `test%s.urbit.org`  
- an urb.py version which uses ports.json

# Todo

## Input handling

- strip ~ and / from ship names

## Variables

- `URBIT` bin/urbit invocation - use for ssh
- `SCREEN` to determine which screen session to run new urbits in, leave blank for direct start in same process (daemon mode maybe?)

## Scripts
- make-vere, make-pill at a commit
- provision gcloud instances
- make-urbit-on
