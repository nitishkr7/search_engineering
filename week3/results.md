CONTAINER ID   IMAGE                                           COMMAND                  CREATED          STATUS                        PORTS                                                                                                      NAMES
0506c4cbb325   opensearchproject/opensearch:2.6.0              "./opensearch-docker…"   27 minutes ago   Up 4 minutes                  9200/tcp, 9300/tcp, 9600/tcp, 9650/tcp                                                                     opensearch-node2
92461b033bc3   opensearchproject/opensearch:2.6.0              "./opensearch-docker…"   27 minutes ago   Up 4 minutes                  9200/tcp, 9300/tcp, 9600/tcp, 9650/tcp                                                                     opensearch-node3
266bbd0ef629   opensearchproject/opensearch:2.6.0              "./opensearch-docker…"   27 minutes ago   Up 4 minutes                  0.0.0.0:9200->9200/tcp, :::9200->9200/tcp, 9300/tcp, 0.0.0.0:9600->9600/tcp, :::9600->9600/tcp, 9650/tcp   opensearch-node1
e6bcc579da32   opensearchproject/opensearch-dashboards:2.6.0   "./opensearch-dashbo…"   27 minutes ago   Up 4 minutes                  0.0.0.0:5601->5601/tcp, :::5601->5601/tcp                                                                  opensearch-dashboards
5fd4bb885a9c   grafana/grafana:9.4.7                           "/run.sh"                2 days ago       Up About a minute             0.0.0.0:3000->3000/tcp, :::3000->3000/tcp                                                                  grafana
d73c9486f163   prom/prometheus:v2.43.0                         "/bin/prometheus --c…"   2 days ago       Up About a minute             0.0.0.0:9090->9090/tcp, :::9090->9090/tcp                                                                  prometheus
7ac2e76a88c6   gcr.io/cadvisor/cadvisor:v0.47.1                "/usr/bin/cadvisor -…"   2 days ago       Up About a minute (healthy)   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp                                                                  cadvisor



ip         heap.percent ram.percent cpu load_1m load_5m load_15m node.role node.roles                                        cluster_manager name
172.18.0.3           59          98  14    2.42    3.35     4.22 dimr      cluster_manager,data,ingest,remote_cluster_client -               opensearch-node2
172.18.0.4           23          98  15    2.39    3.33     4.20 dimr      cluster_manager,data,ingest,remote_cluster_client -               opensearch-node3
172.18.0.5           16          98  14    2.39    3.33     4.20 dimr      cluster_manager,data,ingest,remote_cluster_client *               opensearch-node1


ip         heap.percent ram.percent cpu load_1m load_5m load_15m node.role node.roles                                        cluster_manager name
172.18.0.4           37          95  12    2.17    3.10     4.02 dimr      cluster_manager,data,ingest,remote_cluster_client -               opensearch-node3
172.18.0.3           15          95  12    2.17    3.10     4.02 dimr      cluster_manager,data,ingest,remote_cluster_client *               opensearch-node2


ip         heap.percent ram.percent cpu load_1m load_5m load_15m node.role node.roles                                        cluster_manager name
172.18.0.4           63          99  29    4.20    3.16     3.83 dimr      cluster_manager,data,ingest,remote_cluster_client -               opensearch-node3
172.18.0.5           25          99  31    4.20    3.16     3.83 dimr      cluster_manager,data,ingest,remote_cluster_client -               opensearch-node1
172.18.0.3           37          99  29    4.20    3.16     3.83 dimr      cluster_manager,data,ingest,remote_cluster_client *               opensearch-node2


INFO:Indexing /workspace/search_engineering/product_data/products to bbuy_products with 8 workers, refresh_interval of -1 to host localhost with a maximum number of docs sent per file per worker of 200000 and 500 per batch.
INFO:Done. 1275077 were indexed in 21.705710887365665 minutes.  Total accumulated time spent in `bulk` indexing: 61.61933966211897 minutes

index         shard prirep state     docs   store ip         node
bbuy_products 0     p      STARTED 423938 409.8mb 172.18.0.5 opensearch-node1
bbuy_products 0     r      STARTED 423938 412.4mb 172.18.0.4 opensearch-node3
bbuy_products 0     r      STARTED 423938 416.9mb 172.18.0.3 opensearch-node2
bbuy_products 1     p      STARTED 425833 410.3mb 172.18.0.4 opensearch-node3
bbuy_products 1     r      STARTED 425833 416.4mb 172.18.0.5 opensearch-node1
bbuy_products 1     r      STARTED 425833 416.2mb 172.18.0.3 opensearch-node2
bbuy_products 2     p      STARTED 425306 410.2mb 172.18.0.3 opensearch-node2
bbuy_products 2     r      STARTED 425306 411.4mb 172.18.0.5 opensearch-node1
bbuy_products 2     r      STARTED 425306 413.4mb 172.18.0.4 opensearch-node3


INFO:Indexing /workspace/search_engineering/product_data/products to bbuy_products with 8 workers, refresh_interval of -1 to host localhost with a maximum number of docs sent per file per worker of 200000 and 500 per batch.
INFO:Done. 1275077 were indexed in 15.19394614973183 minutes.  Total accumulated time spent in `bulk` indexing: 24.45480347238481 minutes

index         shard prirep state     docs   store ip         node
bbuy_products 0     p      STARTED 378703 696.3mb 172.18.0.5 opensearch-node1
bbuy_products 1     p      STARTED 377225 490.5mb 172.18.0.4 opensearch-node3
bbuy_products 2     p      STARTED 379522 654.7mb 172.18.0.3 opensearch-node2

66.7s

index         shard prirep state     docs   store ip         node
bbuy_products 0     p      STARTED 423938 411.5mb 172.18.0.5 opensearch-node1
bbuy_products 0     r      STARTED 423938 428.7mb 172.18.0.4 opensearch-node3
bbuy_products 0     r      STARTED 423938 428.8mb 172.18.0.3 opensearch-node2
bbuy_products 1     p      STARTED 425833 423.1mb 172.18.0.4 opensearch-node3
bbuy_products 1     r      STARTED 425833 429.3mb 172.18.0.5 opensearch-node1
bbuy_products 1     r      STARTED 425833   429mb 172.18.0.3 opensearch-node2
bbuy_products 2     p      STARTED 425306 410.3mb 172.18.0.3 opensearch-node2
bbuy_products 2     r      STARTED 425306 428.4mb 172.18.0.5 opensearch-node1
bbuy_products 2     r      STARTED 425306 428.4mb 172.18.0.4 opensearch-node3

138

index                shard prirep state      docs store ip         node
bbuy_products_1shard 0     p      STARTED 1275077 1.7gb 172.18.0.5 opensearch-node1
bbuy_products_1shard 0     r      STARTED 1275077 1.2gb 172.18.0.6 opensearch-node3
bbuy_products_1shard 0     r      STARTED 1275077 1.2gb 172.18.0.8 opensearch-node2
