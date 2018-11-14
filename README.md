# jwtCreator
Creates JWT token

Currently the project can only create JWT token with algo HS256 in header. The library will soon be updated for creation of JWT with multiple algos.

# Use
1. Include the library in the project.
2. Use getToken function with parameters as: header, data, secret key

Example:
  var header = {
    "alg": "HS256",
    "typ": "JWT"
  };
  var data = {
    "username": "Hello World",
    "orig_iat": Math.round((new Date()).getTime() / 1000),
    "exp": Math.round((new Date()).getTime() / 1000) + 604800
  };
  var secret = 'my secret key';
  
  myJWT = getToken(header,data,secret);
