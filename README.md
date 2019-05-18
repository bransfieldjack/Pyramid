# Python Pyramid Setup and Tutorials:
![stem](https://s3-ap-southeast-2.amazonaws.com/stem-formatics/stem_formatics.PNG)
### Setup:

Running on AWS CLoud 9

OS: Ubuntu 18.04.2 LTS
Packages for setup: pip 9.0.1,Python 2.7.15rc1,python-venv

-set an environment variable to where you want your virtual environment.

$ export VENV=~/env

-create the virtual environment.

$ python3 -m venv $VENV

-install pyramid.

$ $VENV/bin/pip install pyramid

-or for a specific released version.

$ $VENV/bin/pip install "pyramid==1.10.4"


### app.py

```
from wsgiref.simple_server import make_server
from pyramid.config import Configurator
from pyramid.response import Response


def hello_world(request):
    return Response('Hello World!')


if __name__ == '__main__':
    with Configurator() as config:
        config.add_route('hello', '/')
        config.add_view(hello_world, route_name='hello')
        app = config.make_wsgi_app()
    server = make_server('0.0.0.0', 6543, app)
    server.serve_forever()
```

The simplest example app, run with '$VENV/bin/python ./app.py'

