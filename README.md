# stripe-test

only did

expo init

expo eject

took App.js, src from https://github.com/expo/expo/tree/master/packages/expo-payments-stripe/examples/with-expokit

Running on android throws 

```
TypeError: TypeError: undefined is not an object (evaluating 'StripeModule.init')

This error is located at:
    in CardFormScreen (at SceneView.js:9)
    in SceneView (at StackViewLayout.js:478)
    in RCTView (at View.js:44)
    in RCTView (at View.js:44)
    in RCTView (at View.js:44)
    in AnimatedComponent (at screens.native.js:59)
    in Screen (at StackViewCard.js:42)
    in Card (at createPointerEventsContainer.js:26)
    in Container (at StackViewLayout.js:507)
    in RCTView (at View.js:44)
    in ScreenContainer (at StackViewLayout.js:401)
    in RCTView (at View.js:44)
    in StackViewLayout (at withOrientation.js:30)
    in withOrientation (at StackView.js:49)
    in RCTView (at View.js:44)
    in Transitioner (at StackView.js:19)
    in StackView (at createNavigator.js:57)
    in Navigator (at createKeyboardAwareNavigator.js:11)
    in KeyboardAwareNavigator (at createNavigationContainer.js:376)
    in NavigationContainer (at withExpoRoot.js:22)
    in RootErrorBoundary (at withExpoRoot.js:21)
    in ExpoRootComponent (at renderApplication.js:34)
    in RCTView (at View.js:44)
    in RCTView (at View.js:44)
    in AppContainer (at renderApplication.js:33)

This error is located at:
    in NavigationContainer (at withExpoRoot.js:22)
    in RootErrorBoundary (at withExpoRoot.js:21)
    in ExpoRootComponent (at renderApplication.js:34)
    in RCTView (at View.js:44)
    in RCTView (at View.js:44)
    in AppContainer (at renderApplication.js:33)
- node_modules/expo-payments-stripe/src/Stripe.js:19:24 in setOptionsAsync
* src/CardFormScreen.js:17:27 in componentWillMount
- node_modules/react-native/Libraries/Renderer/oss/ReactNativeRenderer-dev.js:8145:4 in callComponentWillMount
- node_modules/react-native/Libraries/Renderer/oss/ReactNativeRenderer-dev.js:8286:27 in mountClassInstance
- ... 16 more stack frames from framework internals

```

expo payments fix commit solved the problem

https://github.com/expo/expo/issues/3597#issuecomment-470121059
