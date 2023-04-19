# p2p-metrics

Health metrics for Bitcoin's P2P network

## Metric list

### DNS seed metrics

#### DNS seed summary

The file `dns_seed_summary.csv` contains a summary of the combined node set which is
comprised by the nodes received by all DNS seeds:
- The `total` column indicates the total number of nodes received by all DNS seeds
- The `unique` column represents the number of unique nodes received by all seeds
- The `duplicate` column contains the number of duplicate nodes (i.e. nodes that were
  advertised by multiple peers). When a node is advertised _n_ times, one of the nodes
  is counted as unique; the remaining _n-1_ nodes are counted as duplicates.
- The `reachable` and `unreachable` columns show the number of nodes that could and
  could not be reached. Duplicates are not included in these categories.
- The `stale` column gives the number of nodes that were already received on the
  previous days. Unreachable and duplicate nodes are not included in this category.
- The `pristine` column corresponds to the number of nodes that were unique, reachable
  and not stale (i.e., not part of the previous day's node set).

#### Advertised nodes

The file `dns_seed_advertised_node_count.csv` provides the number of nodes advertised by
each DNS seed.

#### Pristine nodes

The file `dns_seed_pristine_node_count.csv` provides the number of pristine nodes
provided by each DNS seed.

The file `dns_seed_pristine_node_share.csv` holds the share of pristine nodes provided
by each DNS seed (i.e., the ratio of pristine to overall nodes provided by a seed).

#### Stale nodes

The file `dns_seed_stale_node_count.csv` provides the number of stale nodes provided by
each DNS seed.

The file `dns_seed_stale_node_share.csv` holds the share of stale nodes provided
by each DNS seed (i.e., the ratio of stale to overall nodes provided by a seed).

#### Reachable nodes

The file `dns_seed_reachable_node_count.csv` provides the number of reachable nodes
provided by each DNS seed.

The file `dns_seed_reachable_node_share.csv` holds the share of reachable nodes provided
by each DNS seed (i.e., the ratio of reachable to overall nodes provided by a seed).

#### Unreachable nodes

The file `dns_seed_unreachable_node_count.csv` provides the number of unreachable nodes
provided by each DNS seed.

The file `dns_seed_unreachable_node_share.csv` holds the share of unreachable nodes
provided by each DNS seed (i.e., the ratio of unreachable to overall nodes provided by a
seed).

#### Duplicate nodes

The file `dns_seed_duplicate_node_count.csv` provides the number of duplicate nodes
provided by each DNS seed.

The file `dns_seed_duplicate_node_share.csv` holds the share of duplicate nodes provided
by each DNS seed (i.e., the ratio of duplicate to overall nodes provided by a seed).

The number and share of duplicates is calculated based on how many of the nodes
advertised based by a peer were provided by all other seeds.

### P2P metrics

#### Reachable Bitcoin nodes

The file `p2p_reachable_node_count.csv` contains the total number of reachable Bitcoin
nodes, as well as the number of reachable nodes by different network types.

The file `p2p_reachable_node_count.csv` contains the month-over-month (30 days)
percentage change in total number of reachable Bitcoin nodes, as well as the change in
number of reachable nodes by different network types.

The file `p2p_reachable_node_share.csv` comprises the share of nodes contributed by
different network types.
