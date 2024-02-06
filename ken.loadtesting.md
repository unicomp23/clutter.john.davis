kafka topic partitions: 256<br>
msk cluster type: kafka.m5.xlarge<br>
kafka version: 3.3.2<br>
az count: 3<br>
brokers per az: 6<br>
round-trip latency measurement: kafka producer(msk)->kafka consumer(msk)->redis stream(memorydb)<br>
test run time: 30 minutes<br>
producer rate: 1 event/s<br>

| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1kv2.m5.2xlarge.128node.128consumer | 5.0 | 11410.0 | 8.0 | 7.0 | 8.0 | 8.0 | 28.0 | 56.0 | 820.24 | 8767.42 | 126 |
| 1kv2.m5.2xlarge.128node.128consumer | 4.0 | 10220.0 | 7.0 | 6.0 | 7.0 | 7.0 | 27.0 | 68.0 | 888.88 | 4158.82 | 123 |
