# iOS and "JIT"

## What is JIT and why do I care?
JIT stands for **just-in-time compilation**, and (although not specific to Java), it serves as a method of executing Java code quicker then its alternatives, by compiling *essential instructions* at runtime, rather than its slower alternatives that compile *all* code at runtime repeatedly or writing in a less portable, hardware-level format. It is the fastest™ method to running Minecraft: Java Edition on mobile devices, essentially required for a more pleasant gaming experience.

On Apple's mobile platforms (iOS, iPadOS, and _tvOS*_ in our case), a security feature known as **code-signing** is deeply rooted in the operating system. It serves to verify that applications haven't been tampered with after they were installed by a user, done so that malicious payload cannot be installed after-the-fact by a malicious user(e.g. hackers). However, due to the process in which code-signing works, this prevents JIT from functioning properly as it mainly requires reading code, modifying it, and then executing it in some fashion (whether that be by copying the code to a new location in memory, executing directly, or mirroring it).

(*) - tvOS support coming soon!

## What does this mean for Amethyst?

### Jailbroken devices
Users with Jailbroken devices don't need to worry about JIT requirements, as Amethyst is specially built to detect jailbreaks and automatically enable JIT.

### Jailed devices
Users with jailed (unjailbroken) devices can see two different outcomes, based on what they used to sideload Amethyst.

#### TrollStore
If you used TrollStore to sideload Amethyst, good news: Amethyst takes advantage of the extended entitlements granted by TrollStore and automatically enables JIT when launched. **(Turn on URL Schemes)**

#### Normal sideload
If you sideload normally, you will need to enable JIT in some way. The most common method is to attach a debug server to the application while it's running - AltStore, SideStore, StikDebug, SideJITServer, and Jitterbug all use this method to enable JIT. 

The only downside to this method is that you are often required to be connected to a Wi-Fi network or computer in order to enable JIT. 

## What are the methods to enable JIT?

A list of methods and walkthrough to enable JIT for each iOS version can be found [here](https://github.com/C4ndyF1sh/iOS-JIT-Enablers). Additionally, a guide to enabling JIT for Amethyst on iOS 17.4+ follows.

## Enabling JIT for iOS 17.4+ (Jailed):

1. Sideload Angel Aura Amethyst with the `get-task-allow` entitlement. A walkthrough to installing Amethyst with SideStore can be found [here](/getting-started/INSTALL.md).
2. Add the StikDebug Source to SideStore by [tapping here](https://intradeus.github.io/http-protocol-redirector?r=sidestore://source?url=https://stikdebug.xyz/index.json) on your iOS device. Install StikDebug from the source.
3. Set up StikDebug by following the [pairing file guide](https://github.com/StephenDev0/StikDebug-Guide/blob/main/pairing_file.md).
4. On your iOS/iPadOS device, connect to a Wi-Fi network or enable Airplane Mode, then open StikDebug, select "Connect by App", and select Amethyst. You must repeat this step every time you open Amethyst.
5. Congrats, you have successfully enabled JIT for Amethyst.
6. 
