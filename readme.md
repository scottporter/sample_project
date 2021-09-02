# Sample project to demonstrate library setting behavior

After loading the project, type:
```
.libPaths()
```

If you have more than one libPath listed, the behavior is unexpected.

This project has been tested with the following RStudio/R combinatinos:

* RStudio 1.2.5033 and R 3.6.3
   * results are fine (only one libPath)
* RStudio 1.2.1335-1 and R 3.4.1
   * results are not expected (multiple libPaths unless using setHook trick)
* RStudio 1.3.1073-1 and R 3.4.1
   * results are not expected (multiple libPaths unless using setHook trick)
* RStudio 1.3.1073-1 and R 4.0.2
   * results are not expected (multiple libPaths unless using setHook trick)

