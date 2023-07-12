# conan-itk

[ITK](https://itk.org/) C++ libraries installed with Conan C/C++ package manager.

Mostly used to run the conan.io getting started: https://docs.conan.io/en/latest/getting_started.html

## Compiling steps

Change directory to the this folder.


1.  Outputs the source files into the source-folder:

```
conan source .
```

2. Install dependencies:

```
conan install .
```

3.  Build it:

```
conan build .
```

4. Package and export it:

```
conan export-pkg .
```

5. Test it:

You can also test the package that was just exported

```
conan test test_package itk/5.3.0@user/testing
```

