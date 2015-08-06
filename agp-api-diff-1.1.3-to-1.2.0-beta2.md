```diff
diff -U 0 -N gradle-1.1.3_0bfaf44c/com.android.build.gradle.AppPlugin gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.AppPlugin
--- gradle-1.1.3_0bfaf44c/com.android.build.gradle.AppPlugin	2015-08-06 11:05:30.000000000 -1000
+++ gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.AppPlugin	2015-08-06 11:05:37.000000000 -1000
@@ -4 +4 @@
-  public static long __timeStamp__239_neverHappen1425682197386;
+  public static long __timeStamp__239_neverHappen1428701890353;
diff -U 0 -N gradle-1.1.3_0bfaf44c/com.android.build.gradle.BasePlugin gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.BasePlugin
--- gradle-1.1.3_0bfaf44c/com.android.build.gradle.BasePlugin	2015-08-06 11:05:30.000000000 -1000
+++ gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.BasePlugin	2015-08-06 11:05:37.000000000 -1000
@@ -2 +1,0 @@
-  public static final java.lang.String GRADLE_TEST_VERSION;
@@ -6 +5 @@
-  public static long __timeStamp__239_neverHappen1425682197244;
+  public static long __timeStamp__239_neverHappen1428701890328;
@@ -12,0 +12,2 @@
+  public static void access$1(com.android.build.gradle.BasePlugin);
+  public static void access$2(com.android.build.gradle.BasePlugin);
@@ -23 +23,0 @@
-  public com.android.build.gradle.internal.dsl.SigningConfig this$2$getSigningOverride();
diff -U 0 -N gradle-1.1.3_0bfaf44c/com.android.build.gradle.LibraryPlugin gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.LibraryPlugin
--- gradle-1.1.3_0bfaf44c/com.android.build.gradle.LibraryPlugin	2015-08-06 11:05:30.000000000 -1000
+++ gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.LibraryPlugin	2015-08-06 11:05:37.000000000 -1000
@@ -4 +4 @@
-  public static long __timeStamp__239_neverHappen1425682197409;
+  public static long __timeStamp__239_neverHappen1428701890356;
diff -U 0 -N gradle-1.1.3_0bfaf44c/com.android.build.gradle.TestPlugin gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.TestPlugin
--- gradle-1.1.3_0bfaf44c/com.android.build.gradle.TestPlugin	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.2.0-beta2_35a640d9/com.android.build.gradle.TestPlugin	2015-08-06 11:05:37.000000000 -1000
@@ -0,0 +1,30 @@
+public class com.android.build.gradle.TestPlugin extends com.android.build.gradle.BasePlugin implements org.gradle.api.Plugin<org.gradle.api.Project> {
+  public static transient boolean __$stMC;
+  public static long __timeStamp;
+  public static long __timeStamp__239_neverHappen1428701890354;
+  public com.android.build.gradle.TestPlugin(org.gradle.internal.reflect.Instantiator, org.gradle.tooling.provider.model.ToolingModelBuilderRegistry);
+  public void apply(org.gradle.api.Project);
+  public java.lang.Object this$dist$invoke$2(java.lang.String, java.lang.Object);
+  public void this$dist$set$2(java.lang.String, java.lang.Object);
+  public java.lang.Object this$dist$get$2(java.lang.String);
+  public static void __$swapInit();
+  public void apply(java.lang.Object);
+  public java.lang.String super$1$toString();
+  public void super$2$setProperty(java.lang.String, java.lang.Object);
+  public void super$2$createAndroidTasks(boolean);
+  public java.lang.Object super$2$this$dist$invoke$1(java.lang.String, java.lang.Object);
+  public void super$1$wait();
+  public groovy.lang.MetaClass super$2$getMetaClass();
+  public void super$2$setMetaClass(groovy.lang.MetaClass);
+  public void super$2$apply(org.gradle.api.Project);
+  public void super$2$this$dist$set$1(java.lang.String, java.lang.Object);
+  public java.lang.Object super$2$invokeMethod(java.lang.String, java.lang.Object);
+  public java.lang.Object super$2$getProperty(java.lang.String);
+  public void super$1$notifyAll();
+  public void super$2$configureProject();
+  public java.lang.Object super$2$this$dist$get$1(java.lang.String);
+  public groovy.lang.MetaClass super$2$$getStaticMetaClass();
+  public com.android.utils.ILogger super$2$getLogger();
+  public com.android.build.gradle.internal.VariantManager super$2$getVariantManager();
+  public boolean super$2$isLibrary();
+}
```
