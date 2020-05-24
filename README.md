

how to build ios port  
 
#1) building wxWidgets 
build the ios sources in the following way 
- in the wxWidgets folder 
    $mkdir build_ios 
    $cd build_ios
    $../configure --host=i686-apple-darwin_sim --build=x86_64-apple-darwin17.7.0 --with-osx_iphone  --with-macosx-sdk=$(xcrun --sdk iphonesimulator --show-sdk-path) --prefix=<your_prefered_path>
    $make 
    $make install

- in the wxWidgets-ios-cmake folder 
    $mkdir build_ios
    $cd build_ios
    $cmake -G Xcode -DCMAKE_TOOLCHAIN_FILE=../ios.toolchain.cmake -DPLATFORM=SIMULATOR64 ../samples/


