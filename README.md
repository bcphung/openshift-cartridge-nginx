# OpenShift Nginx Cartridge
Welcome to a life where [nginx](http://nginx.org/) is possible on [openshift](https://www.openshift.com/).
 
This cartridge allow you to create a scalable nginx application.
Combine this with the [PHP cartridge](https://github.com/bcphung/openshift-cartridge-php) and you have a scalable application using the latest versions.

Just create your app using:
```BASH
rhc create-app myapp http://cartreflect-claytondev.rhcloud.com/github/bcphung/openshift-cartridge-nginx
```

If you want to install a specific nginx version you can add `--env OPENSHIFT_NGINX_VERSION=<version>` to the command.
For example to install nginx 1.8.0 you can use:
```BASH
rhc create-app myapp --env OPENSHIFT_NGINX_VERSION=1.8.0 http://cartreflect-claytondev.rhcloud.com/github/bcphung/openshift-cartridge-nginx
```

## Versions
Currently this cartridge has the following versions:
- 1.8.0 (latest stable version)
- 1.9.0 (latest mainline version)

If you need another version you can compile it yourself and submit a pull request to get it integrated.
Compile guide is available at [COMPILE.md](https://github.com/bcphung/openshift-cartridge-nginx/blob/master/COMPILE.md)

## Note
This repo only contains _all posible latest versions (stable and mainline)_ of nginx, so what it means to you, let this be said. _This repo will drop the previous one while bump up, so, proceed with caution._
