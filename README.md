# lua-yaml-dump

## 
```
local yaml_dump = require "yaml-dump"
local yaml_str = yaml_dump {
        upstreams = etcd_upstreams.node.nodes
    } .. yaml_dump {
        routes = etcd_routes.node.nodes
    } .. "\n#END"

    print(yaml_str)

```

## 将apisix etcd数据导出到本地文件apisix.yaml
```
init_worker_by_lua_block {
    apisix.http_init_worker()
    require("apisix.own.config-etcd-backup").init_worker()
}
```
