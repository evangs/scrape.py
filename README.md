scrape.py support for multipart forms
=====================================

I needed to submit a multipart form for an automated test.  I enhanced scrape.py to support submission of multipart forms.

How to submit a multipart form
------------------------------
Simply pass in a MultiPartForm object to Session.submit(multipart_data)

example:

>>> data = MultiPartForm()
>>> data.add_field('username', 'john')
>>> data.add_field('password', 'password')
>>> session.submit(form.firsttag('input', name='submit'), params, multipart_data=data)