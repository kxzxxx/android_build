## Android Build System

Use dx desuger toolchain instead of Jack & Jill

Add those to local_manifests

```xml
  <!--Replace build system-->
  <remove-project name="LineageOS/android_build" />
  <project path="build" name="kxzxxx/android_build" groups="pdk">
    <copyfile src="core/root.mk" dest="Makefile" />
  </project>
  
  <!--Replace with 64bit python-->
  <remove-project name="platform/prebuilts/python/linux-x86/2.7.5" />
  <project path="prebuilts/python/linux-x86/2.7.5" 
    name="platform/prebuilts/python/linux-x86/2.7.5" 
    groups="linux,pdk,pdk-cw-fs,pdk-fs" clone-depth="1" remote="aosp"
    revision="826b23851575eece3a3d1ae3bfba73b0060a36f8" />

  ```
