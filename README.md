# rhdh-demo-files
My files used to enhance the RHDH demo

## Quarkus App Catalog Info
This file adds dependencies both resource and component (the POI backend service needs to be created first!)

## Secret
The secret file (not in the repo) is created to be able to pull the RHDH image from Quay.  This is only for pre-release versions (i.e. Dev Preview) as once it is officially released it will go on the publically available RH repo.  Until then use this secret and add the following to the deployment to use this as a pull secret:

``` yaml
spec:
  imagePullSecrets:
    - name: rhdh-pull-secret
  containers:
    - image: 'quay.io/rhdh/developer-hub-rhel9:0.1'
```