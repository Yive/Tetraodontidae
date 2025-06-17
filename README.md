[downloads]: https://ci.yive.dev/job/Pufferfish/
[pluto]: https://github.com/Yive/Pluto
[javadocs]: https://repo.yive.dev/javadoc/snapshots/gg/pufferfish/pufferfish/pufferfish-api/1.21.5-R0.1-SNAPSHOT

# Tetraodontidae
_I was asked to not use the Pufferfish name_

**Note:** This Pufferfish fork is just so that it is easier for me to maintain my optimisation fork called [Pluto][pluto]

A highly optimized Paper fork designed for large servers requiring both maximum performance, stability, and "enterprise" features.

## Features

- **Sentry Integration** Easily track all errors coming from your server in excruciating detail
- **Better Entity Performance** Reduces the performance impact of entities by skipping useless work and making barely-noticeable changes to behavior
- **Partial Asynchronous Processing** Partially offloads some heavy work to other threads where possible without sacrificing stability
- **8x Faster Map Rendering** Reduces or eliminates lag spikes caused by plugins like ImageOnMap or ImageMaps
- **30% faster hoppers** over Paper (Airplane)
- **Reduced GC times & frequency** from removing useless allocations, which also improves CPU performance (Airplane)
- **Fast raytracing** which improves performance of any entity which utilizes line of sight, mainly Villagers (Airplane)
- Faster crafting, reduction in uselessly loaded chunks, faster entity ticking, faster block ticking, faster bat spawning, and more!
- Complete compatibility with any plugin compatible with Paper
- And more coming soon...

## Downloads
You can download the latest JAR file [here][downloads].

## API
You can find the javadocs [here][javadocs].

Maven:
```xml
<repositories>
    <repository>
        <id>yive-repo</id>
        <url>https://repo.yive.dev/snapshots</url>
    </repository>
</repositories>

<dependencies>
    <dependency>
        <groupId>gg.pufferfish.pufferfish</groupId>
        <artifactId>pufferfish-api</artifactId>
        <version>1.21.5-R0.1-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```
Gradle:
```groovy
repositories {
    maven {
        url = 'https://repo.yive.dev/snapshots'
    }
}

dependencies {
    compileOnly 'gg.pufferfish.pufferfish:pufferfish-api:1.21.5-R0.1-SNAPSHOT'
}
```
Paperweight + Gradle KTS:
```kts
repositories {
    maven("https://repo.yive.dev/snapshots")
}

dependencies {
    paperweight.devBundle("gg.pufferfish.pufferfish", "1.21.5-R0.1-SNAPSHOT")
}
```

## Building

```bash
./gradlew applyAllPatches
./gradlew createMojmapPaperclipJar
```

## License
Patches are licensed under GPL-3.0.
All other files are licensed under MIT.
