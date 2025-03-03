django-enforce-host
===================

[![Build Status](https://travis-ci.org/dabapps/django-enforce-host.svg)](https://travis-ci.org/dabapps/django-enforce-host)
[![pypi release](https://img.shields.io/pypi/v/django-enforce-host.svg)](https://pypi.python.org/pypi/django-enforce-host)

Sometimes, it's unavoidable that multiple URLs point at the same app - for example, on Heroku, all apps get a `.herokuapp.com` address, as well as any custom domains that are pointed at them.

This is a simple Django middleware that redirects all traffic from hosts other than the one(s) you specify to your canonical URL.

Tested against Django 2.2, 3.2 and 4.0 on Python 3.6, 3.7, 3.8, 3.9 and 3.10

### Installation

Install from PIP

    pip install django-enforce-host

In your `MIDDLEWARE` setting, add the following at the top:

    MIDDLEWARE = [
        'enforce_host.EnforceHostMiddleware',
        ... other middleware
    ]

Set the following setting to be either a single allowed host, or a list of allowed hosts:

    ENFORCE_HOST = 'yourapp.com'

That's it!

## Code of conduct

For guidelines regarding the code of conduct when contributing to this repository please review [https://www.dabapps.com/open-source/code-of-conduct/](https://www.dabapps.com/open-source/code-of-conduct/)

