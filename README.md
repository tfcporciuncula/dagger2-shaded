[<img src="https://jitpack.io/v/blinkist/dagger2-shaded.svg?style=flat-square">](https://jitpack.io/#blinkist/dagger2-shaded)

# Dagger 2 Shaded 🕶

1. Add this to your build:

```groovy
repositories {
  maven { url "https://jitpack.io" }
}

dependencies {
  implementation 'com.github.blinkist.dagger2-shaded:dagger2-shaded-library:2.x'
  kapt 'com.github.blinkist.dagger2-shaded:dagger2-shaded-compiler:2.x'
}
```

2. Play with Dagger 1 and Dagger 2 at the same time:

```kotlin
class MyClass @Inject @Inject2 constructor() {
  ...
}
```

3. ???

4. Profit.

You can read about this here:
https://fernandocejas.com/2016/08/03/android-dagger-1-and-2-living-together/

Even though that article suggests the [Gradle Shadow Plugin](https://imperceptiblethoughts.com/shadow/), 
I'm using the [Maven Shade Plugin](https://maven.apache.org/plugins/maven-shade-plugin/) 
(which ultimately does the same thing here).

## Updating and building

- Change the `dagger.version` property in the parent POM to the desired value.
- Run `mvn package` to generate the JARs and use them directly in your project.
- ...or make the changes in a fork and use [JitPack](https://jitpack.io/). And open a PR if it's a new version!
