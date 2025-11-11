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

## For Minecraft

To get online functionality working, you will need to follow this guide, exactly as mentioned:  
1) Download [mingw-w64-x86_64-curl](https://mirror.msys2.org/mingw/mingw64/mingw-w64-x86_64-curl-8.17.0-1-any.pkg.tar.zst) and extract it
2) In the extracted folder, rename `mingw64/bin/libcurl-4.dll` to `XCurl.dll`.
3) Copy it to Minecraft's binaries, replacing `XCurl.dll`.
4) Obtain SSL certificates from https://curl.se/ca/cacert.pem and rename this file to `ca-bundle.crt`
5) **IMPORTANT**, Create a folder named `etc`, and under that folder create another folder named `ssl`, and under the `ssl` folder, create a `certs` folder.
6) **IMPORTANT**, Move `ca-bundle.crt` to this new `certs` folder.
if you've done everything correctly, your file structure should look a bit like the following image:
<img width="772" height="240" alt="image" src="https://github.com/user-attachments/assets/d6e27fc3-ecb4-46be-9448-800535bbc1b6" />

Now if you launch the game, the game should be able to phone home and get online. Just keep in mind that `XUser` is still not implemented so no Microsoft Account login yet.   
