# JWT

## Install
```
pip install -r requirements.txt

```

## Run
```
python

import jwt

encoded_jwt = jwt.encode({'some': 'payload'}, 'mysecret', algorithm='HS256')

# Now lets decode it *with a different library*
# Why a different library? Because we want to verify the jwt implementation is correct.

from jose import jwt as jose_jwt

jose_jwt.decode(encoded_jwt, 'mysecret', algorithms=['HS256'])
```
