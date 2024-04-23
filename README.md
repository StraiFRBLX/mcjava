# ☕ mcjava
Just a repository I have made to get Minecraft Java quickly. As always, all of the downloads **are pulled directly from Oracle.** You can see each download link by hovering over the corresponding download buttons. Successor to a website of mine, https://getjava.carrd.co.
<br>If anyone would like to suggest an improvement to this, pull requests are appreciated 🤗
# ⬇️ Downloads
|             Java Version            	|                                                         Windows                                                        	|                                                      MacOS (x86-64)                                                      	|                                                      Linux (x86-64)                                                     	|                                                        Linux (ARM)                                                        	|
|:-----------------------------------:	|:----------------------------------------------------------------------------------------------------------------------:	|:------------------------------------------------------------------------------------------------------------------------:	|:-----------------------------------------------------------------------------------------------------------------------:	|:-------------------------------------------------------------------------------------------------------------------------:	|
| **Java 17**<br>_(1.16.5 and up)_    	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java17-windows-amd64-22.3.1.zip) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java17-darwin-amd64-22.3.1.tar.gz) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java17-linux-amd64-22.3.1.tar.gz) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java17-linux-aarch64-22.3.1.tar.gz) 	|
| **Java 11**<br>_(1.12.2 to 1.16.4)_ 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java11-windows-amd64-22.3.1.zip) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java11-darwin-amd64-22.3.1.tar.gz) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java11-linux-amd64-22.3.1.tar.gz) 	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java11-linux-aarch64-22.3.1.tar.gz) 	|
| **Java 8**<br>_(below 1.12.2)_      	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java8-windows-amd64-21.3.5.zip)  	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java8-darwin-amd64-21.3.5.tar.gz)  	| [⬇️ Download](https://download.oracle.com/otn/utilities_drivers/oracle-labs/graalvm-ee-java8-windows-amd64-21.3.5.zip)   	| X                                                                                                                         	  |
# ❓ What after?
After you have downloaded the necessary Java, here are ways to optimize your game further:
## 💻 Startup Flags
Setting *just the right* startup flags for your minecraft game is a tedious process, and you have to be very careful with what you set. Therefore, I have collected the perfect flags that should improve performance on any machine. However, while the following flags reduce client stutters, expect **only modest FPS** gains at best, and somewhat increased RAM and CPU usage. *(⬇️ See [**here**](https://github.com/brucethemoose/Minecraft-Performance-Flags-Benchmarks?tab=readme-ov-file#flag-explanations:~:text=This%20guide%20assumes,server%20G1GC%20arguments.) if you're constrained by RAM)*

```-XX:+UseG1GC -XX:MaxGCPauseMillis=37 -XX:+PerfDisableSharedMem -XX:G1HeapRegionSize=16M -XX:G1NewSizePercent=23 -XX:G1ReservePercent=20 -XX:SurvivorRatio=32 -XX:G1MixedGCCountTarget=3 -XX:G1HeapWastePercent=20 -XX:InitiatingHeapOccupancyPercent=10 -XX:G1RSetUpdatingPauseTimePercent=0 -XX:MaxTenuringThreshold=1 -XX:G1SATBBufferEnqueueingThresholdPercent=30 -XX:G1ConcMarkStepDurationMillis=5.0 -XX:G1ConcRSHotCardLimit=16 -XX:G1ConcRefinementServiceIntervalMillis=150 -XX:GCTimeRatio=99 -XX:+UnlockExperimentalVMOptions -XX:+UnlockDiagnosticVMOptions -XX:+AlwaysActAsServerClassMachine -XX:+AlwaysPreTouch -XX:+DisableExplicitGC -XX:+UseNUMA -XX:AllocatePrefetchStyle=3 -XX:NmethodSweepActivity=1 -XX:ReservedCodeCacheSize=400M -XX:NonNMethodCodeHeapSize=12M -XX:ProfiledCodeHeapSize=194M -XX:NonProfiledCodeHeapSize=194M -XX:-DontCompileHugeMethods -XX:+PerfDisableSharedMem -XX:+UseFastUnorderedTimeStamps -XX:+UseCriticalJavaThreadPriority -XX:+EagerJVMCI -Dgraal.TuneInlinerExploration=1 -Dgraal.CompilerConfiguration=enterprise```

*To see each flag explained, look [**here!**](https://github.com/brucethemoose/Minecraft-Performance-Flags-Benchmarks?tab=readme-ov-file#flag-explanations)*


## 📈 Performance Modpacks
This is by far the most important and most significant part of the setup. Picking the right mods allows your game to run ***MUCH* faster,** therefore to speed up Minecraft the most, I recommend the following modpacks:
### ✨ [Simply Optimized](https://modrinth.com/modpack/sop) *by HyperSoop*
Best all-round modpack, runs the best out of them all, with the bare minimum needed to optimize your game, no QOL features. I personally use it.
### 💖 [Adrenaline](https://modrinth.com/modpack/adrenaline) *by devin*
Another good contender for the best optimization modpack. Usually used as a "base layer" to build your own modpack upon.
### 💕 [Additive](https://modrinth.com/modpack/additive) *by devin*
The best optifine alternative on Fabric. Most of the OptiFine features are present here, while running stunningly well.


## 💾 Memory Allocation
Minimum and maximum (```-xms``` and ```-xmx```) memory **should be set to the same value,** as explained [**here.**](https://dzone.com/articles/benefits-of-setting-initial-and-maximum-memory-siz)

One exception: if you are on a low-memory system, and Minecraft takes up almost all your RAM, set your minimum memory below your maximum memory to conserve as much as possible.

Sizes are set in **megabytes** (```-Xms4096M```) or **gigabytes** (```-Xmx8G```)

Allocating too much memory can slow Minecraft down, even if you have plenty to spare. Allocating too little can also slow down or break the game. **Keep a close eye** on the Windows Task manager *(or your DE's system monitor)* as Minecraft is running, and allocate ***only as much as it needs** (which is usually less than 8G).*

## ℹ️ Other Tweaks
- *Make sure the Minecraft client is using your discrete GPU!* Check the F3 tab, and force Minecraft to use it in the "Windows Graphics Settings", not the AMD/Nvidia control panel (as they don't seem to work anymore).
- *Close everything in the background!* Yes, even including Discord, as well as game launchers and your browser! Minecraft is resource intensive, and does not like other apps generating CPU interrupts or eating disk I/O, RAM and so on.

### 🫂 Credit
Thanks to [*brucethemoose*](https://github.com/brucethemoose) and their contributors for their [**excellent guide**](https://github.com/brucethemoose/Minecraft-Performance-Flags-Benchmarks) on Minecraft performance tweaking. I took some information from there, so if you need a detailed explanation of any tweak, check it out!
