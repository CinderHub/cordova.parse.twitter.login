## Cordova Parse iOS Twitter Login

## About this Plugin

Parse Twitter Login for an iOS device. Supports iOS Versions 6.0 and up only.

## Using the Plugin

Example:

```
window.iOSTwitterLogin(function (err, session) {
  if (err) return alert(err);
  Parse.User.become(session).then(function (user) {
      // The current user is now set to user.
      console.log('user: ', user);
    }, function (error) {
      // The token could not be validated.
      console.log('error: ', error);
  });
});
```

## Adding the Plugin ##

```
  cordova plugin add https://github.com/nickbarth/cordova.parse.twitter.login.git
```

**NOTE**: You'll also need to configure your Parse and Twitter credentials in your AppDelegate.

```
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    [Parse setApplicationId:@"xxx" clientKey:@"xxx"];
    [PFTwitterUtils initializeWithConsumerKey:@"xxx" consumerSecret:@"xxx"];
    
    return YES;
}
```

## LICENSE ##

The MIT License
