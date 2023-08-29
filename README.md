# Port Information
| Instance | Port Name              | Default Port | Communication Direction    | Description                                                           |
| -------- | ---------------------- | ------------ | -------------------------- | --------------------------------------------------------------------- |
| BE       | be_port                | 9060         | FE -> BE                   | Port of thrift server. For accepting requests which come from FE.     |
| BE       | webserver_port         | 8040         | BE <-> BE                  | Port of http server of BE.                                            |
| BE       | heartbeat_service_port | 9050         | FE -> BE                   | Port heartbeat (thrift) of BE. For accepting heartbeats from FE.      |
| BE       | brpc_port              | 8060         | FE <-> BE, BE <-> BE       | Port of brpc of BE. Used for communication between BE.                |
| FE       | http_port              | 8030         | FE <-> FE, USER -> FE      | Port of http server of FE                                             |
| FE       | rpc_port               | 9020         | BE -> FE, FE <-> FE        | Port of thrift server on FE. Every setting of FE should be consistent |
| FE       | query_port             | 9030         | USER <-> FE                | Port of MySQL server of FE.                                           |
| FE       | edit_log_port          | 9010         | FE <-> FE                  | Port for communication between bdbje of FE.                           |
| Broker   | broker_ipc_port        | 8000         | FE -> BROKER, BE -> BROKER | Port of thrift server of BROKER. For accepting requests.              |

# Connect to Doris with default root user
Doris implements MySQL protocol, so you can use MySQL client to connect to Doris.

- Host: localhost
- Port: 9030
- User: root
- Password: N/A