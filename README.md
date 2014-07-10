shimmozsettings
===============

A shim for Firefox OS mozSettings allowing `addObserver` method.

The shim uses `localStorage` as the replacement of **Settings API** due to the `storage` event. This event is broadcasted to all the windows with the same origin so it's a perfect replacement for the **Settings API**.

Notice `localStorage` is able to store strings only so JSON serialization is used. Furthermore, `localStorage` provides a synchronous API therefore a faked asynchronous API is implemented. Use this Settings replacement to store light settings and not complex objects or embedded files.
