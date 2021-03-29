# lua-yaml-dump

## 
```
local yaml_str = yaml_dump {
        upstreams = etcd_upstreams.node.nodes
    } .. yaml_dump {
        routes = etcd_routes.node.nodes
    } .. "\n#END"

    print(yaml_str)

```
