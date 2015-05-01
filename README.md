TCP Inigo Experiments
=====================


Iperf Experiments
-----------------

This simple experiment was done in [Mininet](http://mininet.org).
Two 30 second iperf flows originating from different hosts,
one arriving 10 seconds before the other, both heading to the same server host.
You can see that TCP Inigo keeps the bottleneck queue on the switch small
while achieving good and fair utilization.

![CDF of bottleneck queue lengths for tech you can expect to use on the WWW](https://raw.githubusercontent.com/systemslab/tcp_inigo_experiments/master/iperf-zoo-n3-bw700-d0.25ms/qlen-cdf-expectedwww.png)


![Inigo iperf throughput](https://raw.githubusercontent.com/systemslab/tcp_inigo_experiments/master/iperf-zoo-n3-bw700-d0.25ms/iperf-inigo.png)

In fact, Inigo behaves similarly to a TCP that has ECN information, even
though it is only using RTTs.

![Bottleneck queue length over time with and without ECN](https://raw.githubusercontent.com/systemslab/tcp_inigo_experiments/master/iperf-zoo-n3-bw700-d0.25ms/qlen-inigo-mimics-ecn-using-rtts.png)

![CDF of bottleneck queue lengths with and without ECN](https://raw.githubusercontent.com/systemslab/tcp_inigo_experiments/master/iperf-zoo-n3-bw700-d0.25ms/qlen-cdf-inigo-mimics-ecn-using-rtts.png)
