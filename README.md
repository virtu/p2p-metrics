# p2p-metrics

Health metrics for Bitcoin's P2P network

## Metric list

### DNS seed metrics

#### Operational summary

The file `dns_seed_categories_node_count.csv` contains a summary of the combined node
set which is comprised by the nodes received by all DNS seeds:
- The `pristine` column corresponds to the number of nodes that were unique, reachable
  and not stale (i.e., not part of the previous day's node set).
- The `stale` column gives the number of nodes that were already received on the
  previous days. Unreachable and duplicate nodes are not included in this category.
- The `unreachable` column lists the number of nodes that could not be reached.
  Duplicates are not included in this category.
- The `unreachable` column contains the number of duplicate nodes (i.e. nodes that were
  advertised by multiple peers). When a node is advertised _n_ times, one of the nodes
  corresponds to an unique node; the remaining _n-1_ nodes are counted as duplicates.

#### Pristine nodes

The file `dns_seed_pristine_node_count.csv` provides a breakdown of the number of
pristine nodes by each individual seed. The file `dns_seed_pristine_node_share.csv`
provides a breakdown of the share of pristine nodes provided by each individual seed. In
addition to per-seed data, the the `overall` column indicates to the number respectively
share of pristine nodes in the set of nodes received by all peers (without duplicates).

#### Stale nodes

The file `dns_seed_stale_node_count.csv` provides a breakdown of the number of stale
nodes by each individual seed. The file `dns_seed_stale_node_share.csv` provides a
breakdown of the share of stale nodes provided by each individual seed. In addition to
per-seed data, the `overall` column indicates to the number respectively share of stale
nodes in the set of nodes received by all peers (without duplicates).

#### Unreachable nodes

The file `dns_seed_unreachable_node_count.csv` provides a breakdown of the number of
unreachable nodes by each individual seed. The file
`dns_seed_unreachable_node_share.csv` provides a breakdown of the share of unreachable
nodes provided by each individual seed. In addition to per-seed data, the `overall`
column indicates to the number respectively share of unreachable nodes in the set of
nodes received by all peers (without duplicates).

#### Duplicate nodes

The file `dns_seed_duplicate_node_count.csv` provides a breakdown of the number of
duplicate nodes by each individual seed. The file `dns_seed_duplicate_node_share.csv`
provides a breakdown of the share of duplicate nodes provided by each individual seed.
The number and share of duplicates is calculated based on how many of the nodes
advertised based by a peer were provided by all other seeds. In addition to per-seed
data, the `overall` column indicates to the number respectively share of duplicate nodes
in the set of nodes received by all peers.
