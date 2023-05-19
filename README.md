# Clustering_Neo4j
```
nano neo4j-enterprise-4.4.18/conf/neo4j.conf
```
add this config in each node
```
#ROLE
dbms.mode=CORE
#CLUSTERING-NODE1
causal_clustering.discovery_type=LIST
causal_clustering.minimum_core_cluster_size_at_formation=3
causal_clustering.minimum_core_cluster_size_at_runtime=2
causal_clustering.initial_discovery_members=10.10.0.2:5000,10.10.0.3:5000,10.10.0.4:5000
causal_clustering.discovery_advertised_address=10.10.0.2:5000
causal_clustering.transaction_advertised_address=10.10.0.2:6000
causal_clustering.raft_advertised_address=10.10.0.2:7000
```
```
#ROLE
dbms.mode=CORE
#CLUSTERING
causal_clustering.discovery_type=LIST
causal_clustering.minimum_core_cluster_size_at_formation=3
causal_clustering.minimum_core_cluster_size_at_runtime=2
causal_clustering.initial_discovery_members=10.10.0.2:5000,10.10.0.3:5000,10.10.0.4:5000
causal_clustering.discovery_advertised_address=10.10.0.3:5000
causal_clustering.transaction_advertised_address=10.10.0.3:6000
causal_clustering.raft_advertised_address=10.10.0.3:7000
```
#ROLE
dbms.mode=CORE
#CLUSTERING-NODE3
causal_clustering.discovery_type=LIST
causal_clustering.minimum_core_cluster_size_at_formation=3
causal_clustering.minimum_core_cluster_size_at_runtime=2
causal_clustering.initial_discovery_members=10.10.0.2:5000,10.10.0.3:5000,10.10.0.4:5000
causal_clustering.discovery_advertised_address=10.10.0.4:5000
causal_clustering.transaction_advertised_address=10.10.0.4:6000
causal_clustering.raft_advertised_address=10.10.0.4:7000
```
<img width="418" alt="image" src="https://github.com/git-raka/Clustering_Neo4j/assets/77326619/04da5d57-654e-4a5f-9093-729f20cd2b3d">
