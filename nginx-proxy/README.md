nginx-proxy
===========

Runs RDMO locally using the script alias `/rdmo`.

### Setup

Add the following to `config/settings/local.py`:

```
BASE_URL = '/rdmo/'
USE_X_FORWARDED_HOST = True
```

Adjust the environment variables in the `Makefile`.

### Usage

Run (in seperate terminals):

```
make gunicorn
make static
docker-compose up
```

RDMO should then be available at http://localhost:8080/rdmo/.
