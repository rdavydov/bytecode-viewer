### Welcome! You have reached the `libs` folder!

#### Adding new dependencies

Run the following command (replacing the placeholders first of course!):
```console
mvn deploy:deploy-file -DgroupId=[GROUP-ID] -DartifactId=[ARTIFACT-ID] -Dversion=[VERSION] -Durl=file:./libs -DrepositoryId=local-maven-repo -DupdateReleaseInfo=true -Dfile=[THE-JAR-FILE]
```

#### Updating dependencies

Just do the same procedure as in "Adding new dependencies", but with a new version number!

You can also safely delete the old version of the dependency, as nothing will depend on it anymore.

#### Why the suffix `bcv`?

Some dependencies may have been modified or could be released by their author in the future. To avoid confusion and dependency clashes in the local repository, the suffix is a nice way to ensure, the right dependency is used in every project (`bcv` = `ByteCode Viewer` btw).

#### Modifications

 - `JD-GUI`: Removed ASM and RSyntaxTextArea
 - `APKTool`: Recompiled with the newest dependency versions, removed prebuilt folder
 - `DarkLAF`: Merged core & windows libraries for 2.6.2-20210719.010320-83