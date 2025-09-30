# create-model-registry

Create a model registry for OpenShift AI. 

The name and namespace of the deployment get used for the database name and namespace respectively.


There is a critical line of code that is buried that needs highlighting. In the MySQL deployment there is a command line argument:
```
--default-authentication-plugin=mysql_native_password
```
The model registry will not work without this line in place!