```diff
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.AppExtension gradle-1.3.0_0996885d/com.android.build.gradle.AppExtension
--- gradle-1.2.3_447fc417/com.android.build.gradle.AppExtension	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.AppExtension	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,5 @@
+public class com.android.build.gradle.AppExtension extends com.android.build.gradle.TestedExtension {
+  public com.android.build.gradle.AppExtension(org.gradle.api.internal.project.ProjectInternal, org.gradle.internal.reflect.Instantiator, com.android.builder.core.AndroidBuilder, com.android.build.gradle.internal.SdkHandler, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.ProductFlavor>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>, com.android.build.gradle.internal.ExtraModelInfo, boolean);
+  public org.gradle.api.internal.DefaultDomainObjectSet<com.android.build.gradle.api.ApplicationVariant> getApplicationVariants();
+  public void addVariant(com.android.build.gradle.api.BaseVariant);
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.AppPlugin gradle-1.3.0_0996885d/com.android.build.gradle.AppPlugin
--- gradle-1.2.3_447fc417/com.android.build.gradle.AppPlugin	2015-08-06 11:05:51.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.AppPlugin	2015-08-06 11:05:54.000000000 -1000
@@ -1 +1 @@
-public class com.android.build.gradle.AppPlugin extends com.android.build.gradle.BasePlugin implements org.gradle.api.Plugin<org.gradle.api.Project> {
+public class com.android.build.gradle.AppPlugin extends com.android.build.gradle.BasePlugin implements org.gradle.api.Plugin<org.gradle.api.Project>, groovy.lang.GroovyObject {
@@ -4 +4 @@
-  public static long __timeStamp__239_neverHappen1430759222558;
+  public static long __timeStamp__239_neverHappen1437758045439;
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.BaseExtension gradle-1.3.0_0996885d/com.android.build.gradle.BaseExtension
--- gradle-1.2.3_447fc417/com.android.build.gradle.BaseExtension	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.BaseExtension	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,113 @@
+public abstract class com.android.build.gradle.BaseExtension implements com.android.build.gradle.AndroidConfig,groovy.lang.GroovyObject {
+  public static transient boolean __$stMC;
+  public static long __timeStamp;
+  public static long __timeStamp__239_neverHappen1437758045362;
+  public com.android.build.gradle.BaseExtension(org.gradle.api.internal.project.ProjectInternal, org.gradle.internal.reflect.Instantiator, com.android.builder.core.AndroidBuilder, com.android.build.gradle.internal.SdkHandler, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.ProductFlavor>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>, com.android.build.gradle.internal.ExtraModelInfo, boolean);
+  public void disableWrite();
+  public void compileSdkVersion(java.lang.String);
+  public void compileSdkVersion(int);
+  public void setCompileSdkVersion(int);
+  public void setCompileSdkVersion(java.lang.String);
+  public void useLibrary(java.lang.String);
+  public void useLibrary(java.lang.String, boolean);
+  public void buildToolsVersion(java.lang.String);
+  public java.lang.String getBuildToolsVersion();
+  public void setBuildToolsVersion(java.lang.String);
+  public void buildTypes(org.gradle.api.Action<? super org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>>);
+  public void productFlavors(org.gradle.api.Action<? super org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.CoreProductFlavor>>);
+  public void signingConfigs(org.gradle.api.Action<? super org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>>);
+  public void flavorDimensions(java.lang.String...);
+  public void sourceSets(org.gradle.api.Action<org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.api.AndroidSourceSet>>);
+  public org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.api.AndroidSourceSet> getSourceSets();
+  public void defaultConfig(org.gradle.api.Action<com.android.build.gradle.internal.dsl.ProductFlavor>);
+  public void aaptOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.AaptOptions>);
+  public void dexOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.DexOptions>);
+  public void lintOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.LintOptions>);
+  public void testOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.TestOptions>);
+  public void compileOptions(org.gradle.api.Action<com.android.build.gradle.internal.CompileOptions>);
+  public void packagingOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.PackagingOptions>);
+  public void preprocessingOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.PreprocessingOptions>);
+  public void jacoco(org.gradle.api.Action<com.android.build.gradle.internal.coverage.JacocoExtension>);
+  public void adbOptions(org.gradle.api.Action<com.android.build.gradle.internal.dsl.AdbOptions>);
+  public void splits(org.gradle.api.Action<com.android.build.gradle.internal.dsl.Splits>);
+  public void deviceProvider(com.android.builder.testing.api.DeviceProvider);
+  public java.util.List<com.android.builder.testing.api.DeviceProvider> getDeviceProviders();
+  public void testServer(com.android.builder.testing.api.TestServer);
+  public java.util.List<com.android.builder.testing.api.TestServer> getTestServers();
+  public void defaultPublishConfig(java.lang.String);
+  public void publishNonDefault(boolean);
+  public java.lang.String getDefaultPublishConfig();
+  public void setDefaultPublishConfig(java.lang.String);
+  public boolean getPublishNonDefault();
+  public void variantFilter(groovy.lang.Closure<java.lang.Void>);
+  public void setVariantFilter(groovy.lang.Closure<java.lang.Void>);
+  public groovy.lang.Closure<java.lang.Void> getVariantFilter();
+  public void resourcePrefix(java.lang.String);
+  public abstract void addVariant(com.android.build.gradle.api.BaseVariant);
+  public void registerArtifactType(java.lang.String, boolean, int);
+  public void registerBuildTypeSourceProvider(java.lang.String, com.android.build.gradle.internal.dsl.BuildType, com.android.builder.model.SourceProvider);
+  public void registerProductFlavorSourceProvider(java.lang.String, com.android.build.gradle.internal.dsl.CoreProductFlavor, com.android.builder.model.SourceProvider);
+  public void registerJavaArtifact(java.lang.String, com.android.build.gradle.api.BaseVariant, java.lang.String, java.lang.String, java.util.Collection<java.io.File>, java.lang.Iterable<java.lang.String>, org.gradle.api.artifacts.Configuration, java.io.File, java.io.File, com.android.builder.model.SourceProvider);
+  public void registerMultiFlavorSourceProvider(java.lang.String, java.lang.String, com.android.builder.model.SourceProvider);
+  public com.android.builder.model.SourceProvider wrapJavaSourceSet(org.gradle.api.tasks.SourceSet);
+  public java.lang.String getCompileSdkVersion();
+  public com.android.sdklib.repository.FullRevision getBuildToolsRevision();
+  public java.util.Collection<com.android.builder.core.LibraryRequest> getLibraryRequests();
+  public java.io.File getSdkDirectory();
+  public java.io.File getNdkDirectory();
+  public java.util.List<java.io.File> getBootClasspath();
+  public java.io.File getAdbExe();
+  public java.io.File getDefaultProguardFile(java.lang.String);
+  public void generatePureSplits(boolean);
+  public void enforceUniquePackageName(boolean);
+  public void setEnforceUniquePackageName(boolean);
+  public boolean getEnforceUniquePackageName();
+  public java.lang.Boolean getPackageBuildConfig();
+  public java.lang.Object this$dist$invoke$1(java.lang.String, java.lang.Object);
+  public void this$dist$set$1(java.lang.String, java.lang.Object);
+  public java.lang.Object this$dist$get$1(java.lang.String);
+  public groovy.lang.MetaClass getMetaClass();
+  public void setMetaClass(groovy.lang.MetaClass);
+  public java.lang.Object invokeMethod(java.lang.String, java.lang.Object);
+  public java.lang.Object getProperty(java.lang.String);
+  public void setProperty(java.lang.String, java.lang.Object);
+  public static void __$swapInit();
+  public final com.android.build.gradle.internal.dsl.ProductFlavor getDefaultConfig();
+  public final com.android.build.gradle.internal.dsl.AaptOptions getAaptOptions();
+  public final com.android.build.gradle.internal.dsl.LintOptions getLintOptions();
+  public final com.android.build.gradle.internal.dsl.DexOptions getDexOptions();
+  public final com.android.build.gradle.internal.dsl.TestOptions getTestOptions();
+  public final com.android.build.gradle.internal.CompileOptions getCompileOptions();
+  public final com.android.build.gradle.internal.dsl.PackagingOptions getPackagingOptions();
+  public final com.android.build.gradle.internal.dsl.PreprocessingOptions getPreprocessingOptions();
+  public final com.android.build.gradle.internal.coverage.JacocoExtension getJacoco();
+  public final com.android.build.gradle.internal.dsl.Splits getSplits();
+  public final org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.CoreProductFlavor> getProductFlavors();
+  public final org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType> getBuildTypes();
+  public final org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig> getSigningConfigs();
+  public final com.android.build.gradle.internal.dsl.AdbOptions getAdbOptions();
+  public java.lang.String getResourcePrefix();
+  public void setResourcePrefix(java.lang.String);
+  public java.util.List<java.lang.String> getFlavorDimensionList();
+  public void setFlavorDimensionList(java.util.List<java.lang.String>);
+  public final org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.api.AndroidSourceSet> getSourceSetsContainer();
+  public boolean getGeneratePureSplits();
+  public boolean isGeneratePureSplits();
+  public void setGeneratePureSplits(boolean);
+  public final java.util.Collection getBuildTypes();
+  public final java.util.Collection getProductFlavors();
+  public final com.android.build.gradle.internal.dsl.CoreProductFlavor getDefaultConfig();
+  public final java.util.Collection getSigningConfigs();
+  public void this$2$ensureTargetSetup();
+  public void super$1$wait();
+  public java.lang.String super$1$toString();
+  public void super$1$wait(long);
+  public void super$1$wait(long, int);
+  public void super$1$notify();
+  public void super$1$notifyAll();
+  public java.lang.Class super$1$getClass();
+  public java.lang.Object super$1$clone();
+  public boolean super$1$equals(java.lang.Object);
+  public int super$1$hashCode();
+  public void super$1$finalize();
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.BasePlugin gradle-1.3.0_0996885d/com.android.build.gradle.BasePlugin
--- gradle-1.2.3_447fc417/com.android.build.gradle.BasePlugin	2015-08-06 11:05:51.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.BasePlugin	2015-08-06 11:05:54.000000000 -1000
@@ -5 +5 @@
-  public static long __timeStamp__239_neverHappen1430759222533;
+  public static long __timeStamp__239_neverHappen1437758045400;
@@ -13 +12,0 @@
-  public static void access$2(com.android.build.gradle.BasePlugin);
@@ -25,0 +25,2 @@
+  public void this$2$checkModulesForErrors();
+  public void this$2$checkPathForErrors();
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.LibraryExtension gradle-1.3.0_0996885d/com.android.build.gradle.LibraryExtension
--- gradle-1.2.3_447fc417/com.android.build.gradle.LibraryExtension	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.LibraryExtension	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,8 @@
+public class com.android.build.gradle.LibraryExtension extends com.android.build.gradle.TestedExtension {
+  public com.android.build.gradle.LibraryExtension(org.gradle.api.internal.project.ProjectInternal, org.gradle.internal.reflect.Instantiator, com.android.builder.core.AndroidBuilder, com.android.build.gradle.internal.SdkHandler, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.ProductFlavor>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>, com.android.build.gradle.internal.ExtraModelInfo, boolean);
+  public org.gradle.api.internal.DefaultDomainObjectSet<com.android.build.gradle.api.LibraryVariant> getLibraryVariants();
+  public void addVariant(com.android.build.gradle.api.BaseVariant);
+  public void packageBuildConfig(boolean);
+  public void setPackageBuildConfig(boolean);
+  public java.lang.Boolean getPackageBuildConfig();
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.LibraryPlugin gradle-1.3.0_0996885d/com.android.build.gradle.LibraryPlugin
--- gradle-1.2.3_447fc417/com.android.build.gradle.LibraryPlugin	2015-08-06 11:05:51.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.LibraryPlugin	2015-08-06 11:05:54.000000000 -1000
@@ -4 +4 @@
-  public static long __timeStamp__239_neverHappen1430759222561;
+  public static long __timeStamp__239_neverHappen1437758045444;
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.TestExtension gradle-1.3.0_0996885d/com.android.build.gradle.TestExtension
--- gradle-1.2.3_447fc417/com.android.build.gradle.TestExtension	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.TestExtension	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,11 @@
+public class com.android.build.gradle.TestExtension extends com.android.build.gradle.BaseExtension implements com.android.build.gradle.TestAndroidConfig {
+  public com.android.build.gradle.TestExtension(org.gradle.api.internal.project.ProjectInternal, org.gradle.internal.reflect.Instantiator, com.android.builder.core.AndroidBuilder, com.android.build.gradle.internal.SdkHandler, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.ProductFlavor>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>, com.android.build.gradle.internal.ExtraModelInfo, boolean);
+  public org.gradle.api.internal.DefaultDomainObjectSet<com.android.build.gradle.api.ApplicationVariant> getApplicationVariants();
+  public void addVariant(com.android.build.gradle.api.BaseVariant);
+  public java.lang.String getTargetProjectPath();
+  public void setTargetProjectPath(java.lang.String);
+  public void targetProjectPath(java.lang.String);
+  public java.lang.String getTargetVariant();
+  public void setTargetVariant(java.lang.String);
+  public void targetVariant(java.lang.String);
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.TestPlugin gradle-1.3.0_0996885d/com.android.build.gradle.TestPlugin
--- gradle-1.2.3_447fc417/com.android.build.gradle.TestPlugin	2015-08-06 11:05:51.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.TestPlugin	2015-08-06 11:05:54.000000000 -1000
@@ -1 +1 @@
-public class com.android.build.gradle.TestPlugin extends com.android.build.gradle.BasePlugin implements org.gradle.api.Plugin<org.gradle.api.Project> {
+public class com.android.build.gradle.TestPlugin extends com.android.build.gradle.BasePlugin implements org.gradle.api.Plugin<org.gradle.api.Project>, groovy.lang.GroovyObject {
@@ -4 +4 @@
-  public static long __timeStamp__239_neverHappen1430759222559;
+  public static long __timeStamp__239_neverHappen1437758045441;
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.TestedExtension gradle-1.3.0_0996885d/com.android.build.gradle.TestedExtension
--- gradle-1.2.3_447fc417/com.android.build.gradle.TestedExtension	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.TestedExtension	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,9 @@
+public abstract class com.android.build.gradle.TestedExtension extends com.android.build.gradle.BaseExtension implements com.android.build.gradle.TestedAndroidConfig {
+  public com.android.build.gradle.TestedExtension(org.gradle.api.internal.project.ProjectInternal, org.gradle.internal.reflect.Instantiator, com.android.builder.core.AndroidBuilder, com.android.build.gradle.internal.SdkHandler, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.BuildType>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.ProductFlavor>, org.gradle.api.NamedDomainObjectContainer<com.android.build.gradle.internal.dsl.SigningConfig>, com.android.build.gradle.internal.ExtraModelInfo, boolean);
+  public org.gradle.api.DomainObjectSet<com.android.build.gradle.api.TestVariant> getTestVariants();
+  public void addTestVariant(com.android.build.gradle.api.TestVariant);
+  public org.gradle.api.DomainObjectSet<com.android.build.gradle.api.UnitTestVariant> getUnitTestVariants();
+  public void addUnitTestVariant(com.android.build.gradle.api.UnitTestVariant);
+  public java.lang.String getTestBuildType();
+  public void setTestBuildType(java.lang.String);
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.internal.ApiObjectFactory gradle-1.3.0_0996885d/com.android.build.gradle.internal.ApiObjectFactory
--- gradle-1.2.3_447fc417/com.android.build.gradle.internal.ApiObjectFactory	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.internal.ApiObjectFactory	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,4 @@
+public class com.android.build.gradle.internal.ApiObjectFactory {
+  public com.android.build.gradle.internal.ApiObjectFactory(com.android.builder.core.AndroidBuilder, com.android.build.gradle.BaseExtension, com.android.build.gradle.internal.variant.VariantFactory, org.gradle.internal.reflect.Instantiator);
+  public void create(com.android.build.gradle.internal.variant.BaseVariantData<?>);
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.internal.NativeLibraryFactoryImpl gradle-1.3.0_0996885d/com.android.build.gradle.internal.NativeLibraryFactoryImpl
--- gradle-1.2.3_447fc417/com.android.build.gradle.internal.NativeLibraryFactoryImpl	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.internal.NativeLibraryFactoryImpl	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,4 @@
+public class com.android.build.gradle.internal.NativeLibraryFactoryImpl implements com.android.build.gradle.internal.model.NativeLibraryFactory {
+  public com.android.build.gradle.internal.NativeLibraryFactoryImpl(com.android.build.gradle.internal.NdkHandler);
+  public com.google.common.base.Optional<com.android.builder.model.NativeLibrary> create(com.android.build.gradle.internal.scope.VariantScope, java.lang.String, com.android.build.gradle.internal.core.Abi);
+}
diff -U 0 -N gradle-1.2.3_447fc417/com.android.build.gradle.internal.dsl.ProductFlavorFactory gradle-1.3.0_0996885d/com.android.build.gradle.internal.dsl.ProductFlavorFactory
--- gradle-1.2.3_447fc417/com.android.build.gradle.internal.dsl.ProductFlavorFactory	1969-12-31 14:00:00.000000000 -1000
+++ gradle-1.3.0_0996885d/com.android.build.gradle.internal.dsl.ProductFlavorFactory	2015-08-06 11:05:54.000000000 -1000
@@ -0,0 +1,5 @@
+public class com.android.build.gradle.internal.dsl.ProductFlavorFactory implements org.gradle.api.NamedDomainObjectFactory<com.android.build.gradle.internal.dsl.ProductFlavor> {
+  public com.android.build.gradle.internal.dsl.ProductFlavorFactory(org.gradle.internal.reflect.Instantiator, org.gradle.api.Project, org.gradle.api.logging.Logger);
+  public com.android.build.gradle.internal.dsl.ProductFlavor create(java.lang.String);
+  public java.lang.Object create(java.lang.String);
+}
```
