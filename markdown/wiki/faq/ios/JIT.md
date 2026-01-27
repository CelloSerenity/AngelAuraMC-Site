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

The methods to enable JIT for each iOS version can be found [here](https://github.com/C4ndyF1sh/iOS-JIT-Enablers).

Methods not listed underneath are not confirmed nor recommended by us for use with Amethyst.

## So how do I enable JIT?

- [TrollStore Lite](https://havoc.app/package/trollstorelite) (!)

- [TrollStore](https://ios.cfw.guide/installing-trollstore) (@)

- [StikDebug](https://stikdebug.xyz/) (^)

- [SideStore](https://docs.sidestore.io/docs/advanced/jit) (*)

- [AltStore AltJIT](https://faq.altstore.io/how-to-use-altstore/altjit) (#)

- [Jitterbug](https://github.com/osy/Jitterbug/tree/main/Jitterbug) ($)

- [SideJITServer](https://github.com/nythepegasus/SideJITServer) (%)



(!) - Limited to Jailbroken devices only. (JIT is granted by the Jailbreak itself)

(@) - Limited to devices with the CoreTrust bug. (iOS 14.0 - iOS 16.7 RC & iOS 17.0)

(^) - iOS 17.4+ only.

(*) - iOS 17.4+, 17.4-18.7.4 only on TXM devices.

(#) - AltJIT for iOS 17.0.1+ betas only works on macOS. Requires pymobiledevice3.

($) - Does not work for iOS 17.0.1+, as enabling JIT will be done with pymobiledevice3.

(%) - Does not work for iOS 16.x or below, use the other methods listed above to enable JIT. This method is meant for iOS 17.0.1-17.3.1 .

