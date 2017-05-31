# ISA Model for Java

The version of this library reflects the version of <https://github.com/ISA-tools/isa-api>. In case the version you wish to use is not available in Central, file a new issue (or pull request).

To use in your project, add mvn dependency

```xml
<dependency>
    <groupId>org.genesys.isa</groupId>
    <artifactId>isa-model</artifactId>
    <version>${isa-api.version}</version>
</dependency>
```

Version info for **isa-api** is in <https://github.com/ISA-tools/isa-api/blob/master/setup.py>

# Updating ISA JSON schemas

Pull from git@github.com:ISA-tools/isa-api.git to a separate directory and check out the version (tag or branch) you wish to use. Create a new branch in this project, replace the schemas in `src/main/resources/schemas` with updated versions from the **isa-api**. Build and package the library.

Tag the library with the version matching your **isa-api** working copy.

# Known issues

1. The <https://github.com/joelittlejohn/jsonschema2pojo> generator creates new Java classes when referenced multiple times. See <https://github.com/joelittlejohn/jsonschema2pojo/issues/623>
2. Generated classnames don't fully respect the naming convention and configuration in `<fileExtensions>` in `pom.xml`. Probably related to #1 above.
