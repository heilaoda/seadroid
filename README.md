# Seafile Android Client [![Build Status](https://secure.travis-ci.org/haiwen/seadroid.png?branch=master)](http://travis-ci.org/haiwen/seadroid)

[![Join the chat at https://gitter.im/haiwen/seadroid](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/haiwen/seadroid?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

The application has been published onto Google Play for easy access:

[![Get it on Google Play](http://www.android.com/images/brand/get_it_on_play_logo_small.png)](https://play.google.com/store/apps/details?id=com.seafile.seadroid2)


## Contributors

See [Contributors Graph](https://github.com/haiwen/seadroid/graphs/contributors)

## Build the APK

* Make sure you have installed Java Development Kit 6 or 7
* Make sure you have installed [Maven](http://maven.apache.org/) 3.1.1+
* Make sure you have installed the [Android SDK](http://developer.android.com/sdk/index.html) then:

```
export ANDROID_HOME=<android SDK location>
export PATH=${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools
echo "y" | android update sdk -a --filter tools,platform-tools,build-tools-20.0.0,android-19 --no-ui --force
```

* Install [Maven Android SDK Deployer](https://github.com/simpligility/maven-android-sdk-deployer) with:

```
cd /tmp/
git clone https://github.com/mosabua/maven-android-sdk-deployer.git
cd maven-android-sdk-deployer
mvn clean install -pl platforms/android-19
```

* Return in `seadroid` directory and build the APK with:

```
mvn clean package
```

You will get `target/seadroid.apk` after the build finishes.

## Develop in Intellij IDEA/Eclipse

### Android Dependencies

* [ActionBarSherlock](https://github.com/JakeWharton/ActionBarSherlock)
* [NewQuickAction](https://github.com/haiwen/NewQuickAction)
* [ViewPagerIndicator](https://github.com/JakeWharton/Android-ViewPagerIndicator)

### Build

- Download `ActionBarSherlock` 4.4.0 from http://actionbarsherlock.com/download.html
- Download `ViewPagerIndicator` 2.4.1 from http://viewpagerindicator.com

- Git clone `NewQuickAction`

        git clone https://github.com/haiwen/NewQuickAction
- Add ActionBarSherlock/NewQuickAction/ViewPagerIndicator as library according to this [referencing library tutorial](http://developer.android.com/guide/developing/projects/projects-eclipse.html#ReferencingLibraryProject)

- Replace the android-support-v4.jar in `ActionBarSherlock` and `ViewPagerIndicator` with the jar in seadroid to make sure that all versions of this library be the same at this time.

- Download these JARs to `seadroid/libs` directory (check pom.xml to verify versions):
    - [http-request-5.6.jar](http://mvnrepository.com/artifact/com.github.kevinsawicki/http-request/5.6)
    - [commons-io-2.4.jar](http://repo1.maven.org/maven2/commons-io/commons-io/2.4/commons-io-2.4.jar)
    - [guava-17.0.jar](http://search.maven.org/remotecontent?filepath=com/google/guava/guava/17.0/guava-17.0.jar)
    - [universal-image-loader-1.9.3.jar](https://raw.githubusercontent.com/nostra13/Android-Universal-Image-Loader/master/downloads/universal-image-loader-1.9.3.jar)

Now you can build seadroid in Intellij IDEA/Eclipse.

## Internationalization

### Contribute your translation

Please submit translations via Transifex: https://www.transifex.com/projects/p/seafile-client/

Steps:

1. Create a free account on Transifex (https://www.transifex.com/).
2. Send a request to join the language translation.
3. After accepted by the project maintainer, then you can upload your file or translate online.
