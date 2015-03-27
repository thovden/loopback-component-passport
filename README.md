# LoopBack Passport Component

** Temporary Branch to workaround lack of support for AngularJS SDK **
The approach is to include AccessToken in successCallback URL using
```
// Include accesstoken if redirect URL has :accessToken in it
  var redirect = successRedirect.replace(/:accessToken/, info.accessToken.id);
  return res.redirect(redirect);
```
**NOTE: This module supersedes [loopback-passport](https://www.npmjs.org/package/loopback-passport). Please update your package.json accordingly.**

The module provides integration between [LoopBack](http://loopback.io) and
[Passport](http://passportjs.org) to support third-party login and account
linking for LoopBack applications.

<img src="./ids_and_credentials.png" width="600px" />

> Please see the [complete documentation](http://docs.strongloop.com/display/LB/Third-party+login) for more information.
