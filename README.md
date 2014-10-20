# python-cf-sample

A barebones Python app, which can easily be deployed to Cloud Foundry.

## Deploying to Cloud Foundry

Clone this repo:
```sh
$ git clone https://github.com/gfoligna/python-cf-sample.git ; cd python-cf-sample
```
Create a MySQL service:
```sh
$ cf create-service cleardb spark python-mysql
```

If you are ready to push, go ahead (:

```sh
$ cf push
```
