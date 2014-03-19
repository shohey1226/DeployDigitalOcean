DeployDigitalOcean
==================

Tools to deploy images to DigitalOcean


### Requirement

```
# deploy image to side a
$ deploy_do --new -image <image_name> -side a -env prod

# without side, creating without side, which can be used for none-side instance, like database
$ deploy_do --new -image <image_name> -env prod

# deploy image with replacing current host
$ deploy_do --replace <hostname/IP> -image <image_name> -env prod

# failover to b side (handled by reverse proxy)
$ failover_a2b
or
$ failver_b2a

# deploy to staging env
# Docker instance is used for this..  <dev host>:<someport> is mapped and user can access
# By default, the instance is stopped and removed in 48 hours
$ deploy_do --new -image <image_name> -env dev 
$ deploy_do --new -image <image_name> -env -dev -live 24 # live for 24 hours
```

