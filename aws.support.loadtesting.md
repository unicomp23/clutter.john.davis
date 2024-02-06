kafka topic partitions: 256<br>
msk cluster type: kafka.m5.xlarge<br>
kafka version: 3.3.2<br>
az count: 3<br>
brokers per az: 6<br>
round-trip latency measurement: kafka producer(msk)->kafka consumer(msk)->redis stream(memorydb)<br>
<br>
<br>
ec2 nodes: 128<br>
per ec2 node: 8 producers, 8 redis stream readers, 1 consumer group worker<br>
| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| base | 6.0 | 18090.0 | 8.0 | 8.0 | 8.0 | 9.0 | 34.0 | 288.59 | 6494.19 | 13141.12 | 116 |
| base | 6.0 | 12801.0 | 9.0 | 8.0 | 9.0 | 9.0 | 34.0 | 241.0 | 6553.36 | 9403.39 | 128 |
| base | 5.0 | 22185.0 | 9.0 | 8.0 | 9.0 | 9.0 | 35.0 | 266.0 | 7199.01 | 14932.76 | 118 |
<br>
<br>
ec2 nodes: 256<br>
per ec2 node: 4 producers, 4 redis stream readers, 1 consumer group worker<br>
| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 256.m5.large.30min | 6.0 | 14768.0 | 8.0 | 8.0 | 8.0 | 9.0 | 28.0 | 56.0 | 1493.16 | 11235.7 | 238 |
| 256.m5.large.30min | 6.0 | 15707.0 | 8.0 | 8.0 | 8.0 | 9.0 | 29.0 | 61.0 | 1361.68 | 5391.51 | 239 |
<br>
<br>
ec2 nodes(client): 256<br>
per ec2 node: 4 producers, 4 redis stream readers<br>
ec2 nodes(worker): 4<br>
per ec2 node: 4 producers, 4 redis stream readers, 4 consumer group worker<br>
| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 256.4cgworkers.30min.m5.large | 5.0 | 8766.0 | 15.0 | 8.0 | 15.0 | 26.0 | 395.0 | 955.0 | 7301.44 | 8249.61 | 223 |
| 256.4cgworkers.30min.m5.large | 5.0 | 12180.0 | 18.0 | 8.0 | 18.0 | 35.0 | 431.0 | 922.0 | 1266.64 | 5932.37 | 221 |
<br>
<br>
ec2 nodes(client): 256<br>
per ec2 node: 4 producers, 4 redis stream readers<br>
ec2 nodes(worker): 16<br>
per ec2 node: 4 producers, 4 redis stream readers, 4 consumer group worker<br>
| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 256.16cgworkers.30min.t3a.small | 5.0 | 34802.0 | 8.0 | 7.0 | 8.0 | 13.0 | 76.0 | 995.0 | 3352.32 | 29984.42 | 222 |
| 256.16cgworkers.30min.t3a.small | 5.0 | 48655.0 | 9.0 | 7.0 | 9.0 | 13.0 | 68.0 | 737.0 | 1225.68 | 30829.39 | 231 |
