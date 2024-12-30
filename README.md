# KPaper

KPaper is a utility library designed to simplify plugin development with [Paper](https://papermc.io/) and [Kotlin](https://kotlinlang.org/). It provides Kotlin-friendly APIs and abstractions to make Paper plugin development faster, cleaner, and more enjoyable.

## Installation

You can add KPaper to your project using the Maven repository hosted by ModLabs.

### Gradle
```kotlin
repositories {
    maven("https://nexus.modlabs.cc/repository/maven-mirrors/")
}

dependencies {
    implementation("cc.modlabs.kpaper:KPaper:$version") // Replace with the desired version
}
```

### Example Usage

Here's a basic example of using KPaper in a plugin:

```kotlin
import de.joker.kpaper.event.listen
import de.joker.kpaper.main.KPlugin
import org.bukkit.event.player.PlayerJoinEvent

class MyPlugin : KPlugin() {
    override fun startup() {
        listen<PlayerJoinEvent> {
            it.player.sendMessage("Welcome to the server, ${it.player.name}!")
        }
    }
}
```

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests on the [GitHub repository](https://github.com/de-joker/kpaper) (replace with actual URL if available).

## Acknowledgments

- [Paper](https://papermc.io/) for providing the high-performance server software.
- [Fruxz](https://github.com/TheFruxz) for the inspiration and libraries that helped shape KPaper.

 
