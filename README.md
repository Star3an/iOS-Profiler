# ios_power_log
A Demo to get cpu power usage on a iOS application(non-jailbreak).

# How to inject library into IPAs
1. Get a decrypted IPA for the app you want to measure. (e.g https://decrypt.day/).
2. Use the dylib I provided or compile it youself (instruction below).
3. Use a ipa inject tool to inject the dylib into the IPA
4. Sign the app and play...

# How to get the log?
1. Open console.app in your Mac
2. Select your Device from left panel.
3. Search for `inject.c: power`. NOTE: The default sample rate is 1/1 second.

# Command to build the dyamic library 
`clang -isysroot $(xcrun --sdk iphoneos --show-sdk-path) -arch arm64 -dynamiclib -lproc -o inject.dylib inject.c`
# Tools to inject dylib into app's macho file.
1. https://github.com/paradiseduo/inject
2. https://github.com/EamonTracey/iPatch (GUI)

![Snipaste_2023-05-10_14-06-15](https://github.com/junjie1475/ios_power_log/assets/86281724/50608ed0-b724-40ed-880e-b71321471569)
