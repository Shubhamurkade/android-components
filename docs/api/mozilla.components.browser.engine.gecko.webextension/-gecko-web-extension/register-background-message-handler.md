[android-components](../../index.md) / [mozilla.components.browser.engine.gecko.webextension](../index.md) / [GeckoWebExtension](index.md) / [registerBackgroundMessageHandler](./register-background-message-handler.md)

# registerBackgroundMessageHandler

`fun registerBackgroundMessageHandler(name: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, messageHandler: `[`MessageHandler`](../../mozilla.components.concept.engine.webextension/-message-handler/index.md)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) [(source)](https://github.com/mozilla-mobile/android-components/blob/master/components/browser/engine-gecko-beta/src/main/java/mozilla/components/browser/engine/gecko/webextension/GeckoWebExtension.kt#L26)

Overrides [WebExtension.registerBackgroundMessageHandler](../../mozilla.components.concept.engine.webextension/-web-extension/register-background-message-handler.md)

Registers a [MessageHandler](../../mozilla.components.concept.engine.webextension/-message-handler/index.md) for message events from background scripts.

### Parameters

`name` - the name of the native "application". This can either be the
name of an application, web extension or a specific feature in case
the web extension opens multiple [Port](../../mozilla.components.concept.engine.webextension/-port/index.md)s. There can only be one handler
with this name per extension and the same name has to be used in
JavaScript when calling `browser.runtime.connectNative` or
`browser.runtime.sendNativeMessage`. Note that name must match
/^\w+(\.\w+)*$/).

`messageHandler` - the message handler to be notified of messaging
events e.g. a port was connected or a message received.