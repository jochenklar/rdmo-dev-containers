export RDMO_APP=${HOME}/code/rdmorganiser/rdmo-app
export SCRIPT_NAME=/rdmo

gunicorn:
	cd ${RDMO_APP}; \
	env/bin/gunicorn --bind 127.0.0.1:9000 --env SCRIPT_NAME=${SCRIPT_NAME} config.wsgi:application

static:
	cd ${RDMO_APP}; \
	env/bin/python manage.py collectstatic --noinput; \
	env/bin/python -m http.server -b 127.0.0.1 -d static_root 9001
