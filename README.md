# python-cf-sample

A barebones Python app, which can easily be deployed to Cloud Foundry.

## Deploying to Cloud Foundry

```sh
$ git clone https://github.com/gfoligna/python-cf-sample.git ; cd python-cf-sample
```

You may want to edit the _manifest.yml_ to change the host name and the service name of your MySQL DB.
The current configuration of the _manifest.yml_ is:

```yaml
---
applications:
- name: python-sample
  instances: 1
  memory: 256M
  path: .
  host: python-sampleee
  command: python manage.py syncdb && gunicorn gettingstarted.wsgi --log-file -
  timeout: 180
  services:
    - python-mysql
```

If you are ready to push, go ahead (:

```sh
$ cf push
```

