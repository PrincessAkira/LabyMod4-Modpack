# LabyMod4-Modpack

My config and modfiles for the Fabric Addon on LabyMod4.
This is subjectivly my Settings so have that in mind.

## How to run this?
- Install [GraalVM](https://github.com/he3als/graalvm-downloader/releases)
- Download the .cmd file and run it
- Select Java 20
- Go into `C:\Program Files\Java` and press Select Folder
- It will ask you what you want to do. Just Press 2 (Extract GraalVM JDK into a new Folder)
- Press Win + R
- Type `gpedit.msc`
- Navigate to `Computer Configuration -> Windows Settings -> Security Settings -> Local Policies -> User Rights Assignments -> Lock Pages in Memory`
- Doubleclick `Lock Pages in Memory`
- `Add User or Group -> Enter your Username in the field -> Press Ok`
- Apply and restart
- Open Minecraft Launcher
- Change JRE Executable to `C:\Program Files\Java\graalvm-jdk20-*ver string*\bin\java.exe`
- As jvm Arguments, set these
```
-Xmx8G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:MaxGCPauseMillis=37 -XX:+PerfDisableSharedMem -XX:G1HeapRegionSize=16M -XX:G1NewSizePercent=23 -XX:G1ReservePercent=20 -XX:SurvivorRatio=32 -XX:G1MixedGCCountTarget=3 -XX:G1HeapWastePercent=20 -XX:InitiatingHeapOccupancyPercent=10 -XX:G1RSetUpdatingPauseTimePercent=0 -XX:MaxTenuringThreshold=1 -XX:G1SATBBufferEnqueueingThresholdPercent=30 -XX:G1ConcMarkStepDurationMillis=5.0 -XX:G1ConcRSHotCardLimit=16 -XX:G1ConcRefinementServiceIntervalMillis=150 -XX:GCTimeRatio=99 -XX:+UnlockDiagnosticVMOptions -XX:+AlwaysActAsServerClassMachine -XX:+AlwaysPreTouch -XX:+DisableExplicitGC -XX:+UseNUMA -XX:AllocatePrefetchStyle=3 -XX:NmethodSweepActivity=1 -XX:ReservedCodeCacheSize=400M -XX:NonNMethodCodeHeapSize=12M -XX:ProfiledCodeHeapSize=194M -XX:NonProfiledCodeHeapSize=194M -XX:-DontCompileHugeMethods -XX:+PerfDisableSharedMem -XX:+UseFastUnorderedTimeStamps -XX:+UseCriticalJavaThreadPriority -XX:+EagerJVMCI -Dgraal.TuneInlinerExploration=1 -Dgraal.CompilerConfiguration=enterprise -Dgraal.UsePriorityInlining=true -Dgraal.Vectorization=true -Dgraal.OptDuplication=true -Dgraal.DetectInvertedLoopsAsCounted=true -Dgraal.LoopInversion=true -Dgraal.VectorizeHashes=true -Dgraal.EnterprisePartialUnroll=true -Dgraal.StripMineNonCountedLoops=true -Dgraal.SpeculativeGuardMovement=true -Dgraal.InfeasiblePathCorrelation=true -XX:+UseLargePages -XX:LargePageSizeInBytes=2m -Dgraal.VectorizeSIMD=true -Dgraal.BaseTargetSpending=160 -XX:MaxTenuringThreshold=1 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:+AlwaysPreTouch -XX:+UseFastStosb -XX:+EliminateLocks
```
- Change the -Xmx8G to whatever RAM size u wanna allocate

