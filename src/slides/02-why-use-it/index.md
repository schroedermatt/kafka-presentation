## Why Kafka?

---

## Use Cases

* Real-time streaming data pipelines
* Real-time streaming applications

<aside class="notes">
- connect any application/system with limited effort
- quickly analyze the data for business value
- transform or react to the streams of data
</aside>

---

## Kafka vs Traditional MOM

* Not your typical message queue
* Offset tracking is moved to the client
* Partitioned topics & consumers groups == scale

<aside class="notes">
- the messages don't go anywhere after being read!
- the broker can move much faster when it has less to worry about
- scaling out consumers with consumer groups is much easier and failover is handled natively
</aside>
