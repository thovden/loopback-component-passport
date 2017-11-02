# LoopBack Passport Component

** Temporary Branch to workaround lack of support for AngularJS SDK **
The original approach was to include AccessToken in successCallback URL using
```
// Include accesstoken if redirect URL has :accessToken in it
  var redirect = successRedirect.replace(/:accessToken/, info.accessToken.id);
  return res.redirect(redirect);

**HOWEVER**, 

we now instead use the cookies set for this purpose. That is the preferred method. 

**Note** that this package works with Loopback 2.x, and the "2.x" versions of this package
depends on Loopback 3.x. 

```


**NOTE: This module supersedes [loopback-passport](https://www.npmjs.org/package/loopback-passport). Please update your package.json accordingly.**

The module provides integration between [LoopBack](http://loopback.io) and
[Passport](http://passportjs.org) to support third-party login and account
linking for LoopBack applications.

<img src="./ids_and_credentials.png" width="600px" />

> Please see the [complete documentation](http://docs.strongloop.com/display/LB/Third-party+login) for more information.
