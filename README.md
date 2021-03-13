
## TuxServer


## API

### Dependency Information
Maven
```xml
<dependency>
    <groupId>me.kingtux.tuxserver</groupId>
    <artifactId>tuxserver-api</artifactId>
    <version>1.16.5-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```



Yes, this also includes all API provided by Purpur, Paper, Spigot, and Bukkit.

## Building and setting up

#### Initial setup
Run the following commands in the root directory:

```
./gradlew applyPatches
```

#### Creating a patch
Patches are effectively just commits in either `TuxServer-API` or `TuxServer-Server`. 
To create one, just add a commit to either repo and run `./gradlew rebuildPatches`, and a 
patch will be placed in the patches folder. Modifying commits will also modify its 
corresponding patch file.

See [CONTRIBUTING.md](CONTRIBUTING.md) for more detailed information.


#### Compiling

Use the command `./gradlew build` to build the api and server. Compiled jars
will be placed under `TuxServer-API/build/libs` and `TuxServer-Server/build/libs`.

To get a TuxServerclip jar, run `./gradlew paperclip`.
To install the `TuxServer-api` and `TuxServer` dependencies to your local maven repo, run `./gradlew publishToMavenLocal`
