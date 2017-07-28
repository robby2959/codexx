# codexx
$ mkdir Frameworks
$ cd Frameworks
$ curl -O https://build.frida.re/frida/ios/lib/FridaGadget.dylib
$ security find-identity -p codesigning -v
  1) A30E15162B3EB979D2572783BF3… "Developer ID Application: …"
  2) E18BA16DF86318F0ECA4BE17C03… "iPhone Developer: …"
     2 valid identities found
$ codesign -f -s E18BA16DF86318F0ECA4BE17C03… FridaGadget.dylib
FridaGadget.dylib: replacing existing signature
