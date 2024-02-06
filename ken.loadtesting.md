kafka topic partitions: 128<br>
msk cluster type: kafka.m5.xlarge<br>
kafka version: 3.3.2<br>
az count: 3<br>
brokers per az: 6<br>
round-trip latency measurement: kafka producer(msk)->kafka consumer(msk)->redis stream(memorydb)<br>
test run time: 30 minutes<br>
producer rate: 1 event/s<br>
<br>
<br>
128 m5.xlarge test driver hosts (producer, end consumer)<br>
16 m5.2xlarge consumer group worker hosts with 8 consumer group workers per hosts (so 128 total worker processes)<br>

| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1kv2.m5.2xlarge.ken | 5.0 | 4161.0 | 9.0 | 8.0 | 9.0 | 11.0 | 48.0 | 1519.0 | 2130.04 | 3586.93 | 134 |
<br>
<br>
initial load test<br>
| Directory | Min | Max | Median | 25th percentile | 50th percentile | 75th percentile | 99th percentile | 99.9th percentile | 99.99th percentile | 99.999th percentile | JSON File Count |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1kv2.m5.2xlarge.128node.128consumer | 5.0 | 11410.0 | 8.0 | 7.0 | 8.0 | 8.0 | 28.0 | 56.0 | 820.24 | 8767.42 | 126 |
| 1kv2.m5.2xlarge.128node.128consumer | 4.0 | 10220.0 | 7.0 | 6.0 | 7.0 | 7.0 | 27.0 | 68.0 | 888.88 | 4158.82 | 123 |
