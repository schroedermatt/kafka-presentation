
![what the heck](./images/what-the-heck.jpg)

---

Apache Kafka is an <span style="color:#c82506">**open source**</span> distributed streaming platform capable of handling <span style="color:#c82506">**[trillions](https://www.confluent.io/blog/apache-kafka-hits-1-1-trillion-messages-per-day-joins-the-4-comma-club)**</span> of events a day. Initially conceived as a messaging queue, Kafka is based on an abstraction of a <span style="color:#c82506">**distributed commit log**</span>. Since being created and open sourced by LinkedIn in 2011, Kafka has quickly evolved from messaging queue to a full-fledged <span style="color:#c82506">**streaming platform**</span>.</br><span style="font-size: 16px">_[Confluent - What is Kafka?](https://www.confluent.io/what-is-apache-kafka/)_</span>

---

<span style="color:#c82506">**Apache Kafka is**</span>
<span style="color:#B3B3B3">~~an open source distributed streaming platform capable of handling trillions of events a day. Initially conceived as a messaging queue, Kafka is based on an abstraction of~~</span>
<span style="color:#c82506">**a distributed commit log**</span>
<span style="color:#B3B3B3">~~.Since being created~~</span>
<span style="color:#c82506">**and open sourced**</span>
<span style="color:#B3B3B3">~~by LinkedIn in 2011, Kafka has quickly evolved from messaging queue to a full-fledged~~</span>
<span style="color:#c82506">**streaming platform.**</span>

---

## Core Concepts

* Streams of _records_ are stored in _topics_
* Topics are partitioned and replicated across _brokers_

![topic anatomy](./images/topic-anatomy.png)

<aside class="notes">

* Each record has a key, value, and timestamp
* The message key determines the assigned _partition_
* Partitions are a sequence of messages with an _offset_
  * Offset is a consumer's bookmark

</aside>

---

## Guarantees

* Ordering of messages within a partition
* Consumers see records in order
* A topic will not lose data unless N brokers fail
  * _N == replication factor_

<aside class="notes">
* Messages sent by a producer to a particular topic partition will be appended in the order they are sent.
* A consumer instance sees records in the order they are stored in the log.
* For a topic with replication factor N, N-1 servers can fail without losing any records.
  
* Kafka is scalable
* Kafka is durable
* Kafka is blazing fast
  
</aside>
