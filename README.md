# Usage

### Please use the following code:

```
module "app1" {
  source    = "AliAQ9/release1/helm"
  namespace = "default"
  name      = "wordpress"
  wait      = false
  chart     = "./application"
  values = []
}
```