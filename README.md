This repository includes all the benchmarks used to evaluate ART GC:  
1- BufferBench, which creates objects in the memory or reads the objects from the memory.   
2- Etalon-DaCapo is a port of a set of DaCapo Java Benchmark to Android devices. It is downloaded from: https://github.com/fizous/etalondacapo
But the SDK version changed to 30  
3- The APKs for CPDT, MarkPass PerformanceTest Mobile, and CF_bench  
All the benchmarks were tested on a Google Pixel 3A  with 2 GB RAM, 15 GB disk, and running Android 11.   
To run the BufferBench and Etalon-DaCapo open them in Android Studio IDE using OpenJDK 15 and SDK version 30 for the latest version of Android, 11(R) (as of writing this document).  
To get the GC information during running a specific application:  
1- Execute the following command to use adb shell:  
```
adb shell
su
kill -s QUIT  #PID \\Process ID of running application
```
2- The above command creates a file in `\data\anr` directory on the emulator.
