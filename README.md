# Getting Started

Create a Podfile in the root directory of your project.

``` ruby
$ pod init
```

Add Official CocoaPods PodSpecs repository to your Podfile:
``` ruby
source 'https://github.com/CocoaPods/Specs.git'
```

Add Discover-Tech PodSpecs repository to your Podfile:

``` ruby
source 'https://github.com/dekelboni/DT-iOS-SDK/DT-SDk_specs.git'
```

Using terminal, with your project root directory as the working path, run:

``` ruby
pod install
# pod update (use this when you want to get new released version).
```


The app should supply few user's info for getting the best results, by implementing this protocol:



``` swift

// Optional 
struct Location {
    var longitude: Double!
    var latitude: Double!
}

protocol UserDataProvider {
    var userName: String { get }
    var userEmail: String { get }
    var phoneNumber: String { get }
    var location: Location { get }
}
```

On your `SceneDelegate` in the `sceneDidBecomeActive` method add:

``` swift

DTTracker.launchApp({APP_ID})
```
