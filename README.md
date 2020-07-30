Etcd Watcher
====

Etcd Watcher is the [Etcd](https://github.com/coreos/etcd) watcher for [PyCasbin](https://github.com/casbin/pycasbin). With this library, Casbin can synchronize the policy with the database in multiple enforcer instances.

## Installation

    pip install Etcd_watcher

## Simple Example

Example used along with https://github.com/pycasbin/flask-authz
```
from flask_authz import CasbinEnforcer
from casbin_redis_watcher import RedisWatcher
casbin_enforcer = CasbinEnforcer(app, adapter)
watcher=RedisWatcher(redis_hostname, redis_port)
watcher.set_update_callback(casbin_enforcer.e.load_policy)
casbin_enforcer.set_watcher(watcher)

```

## Getting Help

- [PyCasbin](https://github.com/casbin/pycasbin)

## License

This project is under Apache 2.0 License. See the [LICENSE](LICENSE) file for the full license text.
