Proof of Concept loading lnd CGO falafel bindings into an Electron app via a
NodeJS C++ addon.

* Clone cshared branch: https://github.com/hsjoberg/lnd/tree/cshared
* Run `make cgo`
* Rename `mobile/build/cgo/mobile` to `liblnd.{a,so,dll}` depending on your
platform and copy it over to root of this project.
* Run `yarn start` start up dev mode or `yarn package` to build the app

To cross-compile, first get the correct platform-specific liblnd file and then
run `TARGET_PLATFORM={darwin,linux,win32} yarn package --platform {darwin,linux,win32}`
Replace `{darwin,linux,win32}` with the platform you want to build for.
