# consul-service-discovery-demo

Demonstration of using service discovery using Consul.

## Useful commands:

Init server mode

`consul agent -server -bootstrap-expect=3 -node=consulserver03 -bind=172.17.0.3 -data-dir=/var/lib/consul -config-dir=/etc/consul.d`

Init client mode

`consul agent -bind=172.17.0.5 -data-dir=/var/lib/consul -config-dir=/etc/consul.d`

Reload context

`consul reload`

List members

`consul members`

Registry node

`consul join 172.17.0.3`

Init agent and join with config file

`consul agent -bind=172.17.0.6 -data-dir=/var/lib/consul -config-dir=/etc/consul.d -retry-join=172.17.0.3`

> Based on course content by Wesley Williams
