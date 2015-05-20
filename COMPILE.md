# Openshift Nginx Cartridge - Compile guide

### Compiling a new version
- To compile a new version you will first need a OpenShift application.
```BASH
rhc create-app nginx http://cartreflect-claytondev.rhcloud.com/github/boekkooi/openshift-cartridge-nginx
```
- Clone the repository and create a `nginx` folder.
- Copy the `usr/compile` directory from [this](https://github.com/boekkooi/openshift-cartridge-nginx) repository.
- Set the versions you need to compile in the `nginx/compile/versions` file. Commit and push the application repository.
- SSH into you app and go to the `nginx/compile` folder and start compiling by running the following command:
```BASH
cd ${OPENSHIFT_REPO_DIR}/nginx/compile
./all
```
- Once compiling is done you can download the `nginx.tar.gz` from your application. 
- Extract the `nginx-{version}` from the archive and place them into the `openshift-cartridge-nginx/usr` folder.
- Last but not least edit the `openshift-cartridge-nginx/manifest.yml` and add the versions.
- All done just commit and push to your `openshift-cartridge-nginx` repo and use:
```BASH
http://cartreflect-claytondev.rhcloud.com/github/<user>/openshift-cartridge-nginx
```
