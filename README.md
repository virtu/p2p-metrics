# p2p-metrics

Health metrics for Bitcoin's P2P network

## Metric list

### DNS seed metrics

- Number of advertised nodes (`dns_seed_advertised_node_count.csv`)
  - The `overall` field corresponds to the sum of the number of nodes received by
    indivudal DNS seeds
  - The `unique` field records the number of `unique` nodes received by all seeds.
  - The remaning fields, named after individual DNS seeds, indicate the number of nodes
    received from individual seeds.
