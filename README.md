# loopback-component-passport

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

> Please see the [official documentation](http://docs.strongloop.com/pages/viewpage.action?pageId=3836277) for more information.

## All local accounts requires verification

### All third party accounts will login with an email of `uniqueID@loopback.provider.com` example `123456@loopback.facebook.com`

which will allow the user to link the social media accounts that they want as well as the users could sign up with the same email account that is used for facebook/twitter/google/local if they wish to keep them separate.

Facebook profile information (such as email, gender, timezone, etc) may still be included if necessary. See
https://github.com/strongloop/loopback-example-passport/blob/master/README.md#4-facebook-profile-info.

All user required info including the email will be available, but the main email for the account will remain `uniqueID@loopback.facebook.com`.
