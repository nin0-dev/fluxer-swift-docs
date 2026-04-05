---
order: "300"
---
## Prerequisites
To get started, you'll want:
- a macOS or Linux install;
- the [Swift programming language](https://swift.org) installed;
- some knowledge of that language.

> [!warning] Windows support
> No testing is done on Windows, as I do not have a Windows machine. This means that **you are on your own** if you have any issues, unless they also happen on a supported platform.
> 
> However, you can (and should) use WSL to use Swift on Windows.

## Initialize package
Make a folder for your bot, and run the following command in your terminal:
```sh
swift package init --type executable
```
You may also want to initialize a Git repo, to keep track of your changes:
```sh
git init
```
## Add `fluxer-swift`
You'll want to add `fluxer-swift` as a package dependency, then as a dependency on your target. Your `Package.swift` should look like this:
```swift
import PackageDescription

let package = Package(
    name: "name",
    dependencies: [
	    .package(url: "https://github.com/nin0-dev/fluxer-swift", from: "1.0.0"),
	],
    targets: [
        .executableTarget(
            name: "name"
            dependencies: [
                .product(name: "FluxerSwift", package: "fluxer-swift")
            ]
        ),
    ]
)
```
