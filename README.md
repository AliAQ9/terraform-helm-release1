# Usage

### Please use the following code:

```
module "app1" {
  source    = "AliAQ9/release/helm"
  namespace = "default"
  name      = "wordpress"
  wait      = false
  chart     = "./application"
  values = [<<EOF
  
    replicaCount: 3

image:
  repository: wordpress
  pullPolicy: IfNotPresent
  tag: "latest"

  EOF
  ]
}
```