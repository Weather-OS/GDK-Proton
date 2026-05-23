# GDK-Proton
This repository aims to share builds of GE-Proton, custom built with WineGDK and several extra components.
```
mingw-w64-x86_64-brotli
mingw-w64-x86_64-c-ares
mingw-w64-x86_64-ca-certificates
mingw-w64-x86_64-cc-libs
mingw-w64-x86_64-libidn2
mingw-w64-x86_64-libpsl
mingw-w64-x86_64-libssh2
mingw-w64-x86_64-nghttp2
mingw-w64-x86_64-nghttp3
mingw-w64-x86_64-ngtcp2
mingw-w64-x86_64-openssl
mingw-w64-x86_64-zlib
mingw-w64-x86_64-zstd
mingw-w64-x86_64-gettext-runtime
mingw-w64-x86_64-libiconv
mingw-w64-x86_64-libunistring
xgameruntime.dll.threading
```

## For games using `XCurl.dll`

**NOTES**: OpenSSL only works in protonified wine builds. You can use GDK-Proton (in the Releases section of this Repository) if you are not inclined to build proton from scratch yourself.

To get online functionality working, use the `replace-xcurl` script in this repo, syntax:

```sh
./replace-xcurl [path/to/game]
```

Now if you launch the game, the game should be able to phone home and get online. Just keep in mind that `XUser` is still not implemented so no Microsoft Account login yet.
