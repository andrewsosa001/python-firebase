python-firebase
===============
http://github.com/mikexstudios/python-firebase
by Michael Huynh (mike@mikexstudios.com)

https://github.com/omenar/python-firebase
by Osvaldo Mena

Purpose:
-------

A very simple wrapper for Firebase's REST API.

How to use
----------

Import firebase at the top of your python script:

        from firebase import Firebase

and then instantiate Firebase, passing in your root url:

        f = Firebase('https://SampleChat.firebaseIO-demo.com/')

You may optionaly pass a [Firebase authentication token](https://www.firebase.com/docs/security/custom-login.html) to secure your calls:

        f = Firebase('http://SampleChat.firebaseIO-demo.com/', auth_token="<my_firebase_auth_token>")

Now call the different methods of the Firebase class (see the Firebase
REST API page: http://www.firebase.com/docs/rest-api.html and the source of
`firebase/__init__.py` for what methods are available and how to call
them). For example, to push a list of data:

        f = Firebase('https://SampleChat.firebaseIO-demo.com/message_list')
        r = f.push({'user_id': 'wilma', 'text': 'Hello'})

The response `r` is a dictionary containing Firebase's REST response:

        {"name":"-INOQPH-aV_psbk3ZXEX"}


License
-------

python-firebase is BSD licensed.
See License file. 

