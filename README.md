# Grails Plugin Demo

Grails plugin demo, use `org.grails.internal.grails-plugin-publish` to publish it.

## Grails Version

- Grails **5.1.2**

## Usage

To publish this new plugin to local maven repository, 
first, we should set project version `0.1-SNAPSHOT`, because only **Snapshot** plugin could be published to local maven repository.
then, add `org.grails.internal.grails-plugin-publish` to `build.gradle`.

```
apply plugin:"org.grails.internal.grails-plugin-publish"
```

and most important, provide a valid publishing configuration,

```
grailsPublish {
    user = 'rainboyan'
    key = 'grails-new-plugin-demo'
    githubSlug = 'rainboyan/grails-new-plugin-demo'
    license {
        name = 'Apache-2.0'
    }
    title = "Grails new plugin demo"
    desc = "My plugin description"
    developers = [rainboyan:"Michael Yan"]
}
```

### Build and Install

```
git clone https://github.com/rainboyan/grails-new-plugin-demo.git
cd grails-new-plugin-demo
./gradlew install
or
./gradlew publishToMavenLocal
```

## Links

- [Grails](https://grails.org)
- [Grails Github](https://github.com/grails)
- [Grails Gradle Plugin](https://github.com/grails/grails-gradle-plugin/)
- [Grails Plugins Doc](https://docs.grails.org/latest/guide/plugins.html#creatingAndInstallingPlugins)
