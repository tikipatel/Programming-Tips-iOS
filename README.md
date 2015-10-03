# Programming-Tips-iOS
A list of tricks and tips for iOS programming

##Debugging

###Views


#### `-recursiveDescription`
Sometimes we want want see the view hierarchy in lldb. We can access private / undocumented Objective-C API `-recursiveDescription` to achieve this as shown below.

For Swift projects: 

```lldb-swift
expr -l objc++ -O -- [[UIWindow keyWindow] recursiveDescription]
```

For Objective-C projects:

```lldb-objc
[[UIWindow keyWindow] recursiveDescription]
```
