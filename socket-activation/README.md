# Socket Activation Example
The following is an example of how I've setup socket activation for pgAdmin using `systemd-socket-proxyd`
to proxy requests

`pgadmin-proxy.socket` sets up the port 5555 as `ListenStream` that starts `pgadmin-proxy.service` when connection
is established. `pgadmin-proxy.service` will then kick off `pgadmin.service`

