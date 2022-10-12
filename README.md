# conan-itk

[ITK](https://itk.org/) C++ libraries installed with Conan C/C++ package manager.

Mostly used to run the conan.io getting started: https://docs.conan.io/en/latest/getting_started.html

## Compiling steps

1.  Outputs the source files into the source-folder:

```
conan source  . --source-folder=tmp/source
```

2. Install dependencies:

```
conan install . --install-folder=tmp/build
```

3.  Build it:

```
conan build   . --source-folder=tmp/source --build-folder=tmp/build
```

4. Package it:

```
conan package . --source-folder=tmp/source --build-folder=tmp/build --package-folder=tmp/package
```

5. Export it:

Use --force to prevent ERROR: Package already exists

```
conan export-pkg . user/testing --source-folder=tmp/source --build-folder=tmp/build --force
```

6. Test it:

You can also test the package that was just exported

```
conan test test_package itk/5.2.1@user/testing
```

7. Finally, run a full create, does all of the above + test_package

```
conan create . user/testing
```
