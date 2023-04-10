# Maktabaty Documentation
[![](https://scontent.falg7-2.fna.fbcdn.net/v/t39.30808-6/340238644_185488260959029_5111790709240297752_n.jpg?_nc_cat=100&ccb=1-7&_nc_sid=730e14&_nc_ohc=GGRHRqi6GtwAX-51kZ-&_nc_ht=scontent.falg7-2.fna&oh=00_AfBQZtuEes0fp646q7v8bLcFo6WHmISTmqz-E0wJlmXFKA&oe=64338B3C)](https://www.linkedin.com/in/hakodridi/)
## What is makatabaty ?
Maktabaty is an Android application for the digital version of the schools books 

## Installation
### Android app :
 1. Load the project (source code) to your IDE ( Android Studio).
    > File->Open
 2. Modify the content of Gradle files concerning your version.
 and here a example :
     > build.gradle
     > from
 ```gradle
buildscript {  
  repositories {  
  
  maven {  
  url "https://jitpack.io"  
  }  
  
 }  dependencies {  
  classpath 'com.novoda:bintray-release:0.9'  
  classpath 'com.google.gms:google-services:4.3.13'  
  classpath "com.jfrog.bintray.gradle:gradle-bintray-plugin:1.8.4"  
  classpath 'com.github.dcendents:android-maven-gradle-plugin:2.1'  
  classpath 'gradle.plugin.com.onesignal:onesignal-gradle-plugin:0.14.0'  
  }  
}  
plugins {  
  id 'com.android.application' version '7.0.2' apply false  
  id 'com.android.library' version '7.0.2' apply false  
}  
  
task clean(type: Delete) {  
  delete rootProject.buildDir  
}
```
> to this one
```gradle
plugins {  
  id 'com.android.application' version '7.3.1' apply false  
  id 'com.android.library' version '7.3.1' apply false  
}
```

### Server side
> There's no source code now

## Used libraries 
1. **Android default libraries**
    ```gradle
    implementation 'androidx.appcompat:appcompat:1.4.1'
    ```
    ```gradle
    implementation 'com.google.android.material:material:1.6.1'
    ```
    ```gradle
    implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
    ```
    ```gradle
    implementation 'com.google.firebase:firebase-database:20.0.5'
    ```
    ```gradle
    implementation 'com.google.firebase:firebase-messaging:23.0.8'
    ```
    ```gradle
    testImplementation 'junit:junit:4.13.2'
    ```
    ```gradle
    androidTestImplementation('androidx.test:runner:1.1.0-alpha4', {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
    ```
    ```gradle
    androidTestImplementation('androidx.test.espresso:espresso-core:3.1.0-alpha4', {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
    ```
    ```gradle
    implementation 'com.google.android.play:core:1.10.3' 
    ``` 
    ```gradle
    implementation 'androidx.multidex:multidex:2.0.1'
    ```
    ```gradle
    implementation 'androidx.palette:palette:1.0.0'
    ```
    ```gradle
    implementation 'commons-io:commons-io:2.4'
    ```
    ```gradle
    def room_version = "2.3.0"  
    implementation "androidx.room:room-runtime:$room_version"  
    annotationProcessor "androidx.room:room-compiler:$room_version"  
    implementation "androidx.room:room-rxjava2:$room_version"  
    implementation "androidx.room:room-rxjava3:$room_version"  
    implementation "androidx.room:room-guava:$room_version"  
    testImplementation "androidx.room:room-testing:$room_version"
    ```
    ```gradle
    androidTestImplementation 'androidx.test.ext:junit:1.1.3'  
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.4.0'
    ```
    
2. **File library (nemosofts)**
    ```gradle
    implementation files('libs/nemosofts.aar')
    ```
3. **Imported libraries**
    - <a href="https://github.com/google/gson" target="_blank">*Gson*</a> is a Java library that can be used to convert Java Objects into their JSON representation
    ```gradle
    implementation 'com.google.code.gson:gson:2.9.0'
    ```
    
    - <a href="https://github.com/square/picasso" target="_blank">*Picasso*</a> : A powerful image downloading and caching library for Android
        ```gradle
        implementation 'com.squareup.picasso:picasso:2.71828'
        ```

    - <a href="https://github.com/vinc3m1/RoundedImageView" target="_blank">*RoundedImageView*</a> was originally made with a primary goal of memory and rendering performance, and specifically only worked well on Bitmaps. It had some very poorly performing hacks built in for non-bitmaps, along with a lot of hard to maintain synchronization of ScaleTypes and sizing between the ImageView and the Drawable itself.
        ```gradle
        implementation 'com.makeramen:roundedimageview:2.3.0'
        ```

    - <a href="https://github.com/GrenderG/Toasty" target="_blank">*Toasty*</a>
        ```gradle
        implementation 'com.github.GrenderG:Toasty:1.5.2'
        ```

    - <a href="https://github.com/castorflex/SmoothProgressBar" target="_blank">*SmoothProgressBarView*</a> is a small library allowing you to make a smooth indeterminate progress bar
        ```gradle
        implementation 'com.github.castorflex.smoothprogressbar:library-circular:1.3.0'
        ```

    - <a href="https://github.com/yakivmospan/scytale" target="_blank">*Scytale*</a> : one tool to manage key generation, key storing and encryption on different APIs of Android.
        ```gradle
        implementation 'com.yakivmospan:scytale:1.0.1'
        ```

    - <a href="https://github.com/journeyapps/zxing-android-embedded" target="_blank">*ZXing*</a> : barcode scanning library for Android, using ZXing for decoding.
        ```gradle
        implementation 'com.journeyapps:zxing-android-embedded:4.1.0'
        ```

    - <a href="https://github.com/barteksc/AndroidPdfViewer" target="_blank">*PdfViewer*</a> : library for displaying PDF documents on Android, with animations, gestures, zoom and double tap support.
        ```gradle
        implementation 'com.github.barteksc:pdf-view-pager:1.0.3'
        ```

    - <a href="https://google.github.io/volley/" target="_blank">*Volley*</a> is an HTTP library that makes networking for Android apps easier and most importantly, faster.
        ```gradle
        implementation 'com.android.volley:volley:1.2.1'
        ```

    - <a href="https://github.com/umano/AndroidSlidingUpPanel" target="_blank">*Android Sliding Up Panel*</a> : this library provides a simple way to add a draggable sliding up panel (popularized by Google Music and Google Maps) to your Android application.
        ```gradle
        implementation 'com.sothree.slidinguppanel:library:3.4.0'
        ```

    - <a href="https://github.com/lizhangqu/CoreProgress" target="_blank">*CoreProgress*</a> is a framework to support OkHttp upload and download progress
        ```gradle
        implementation 'io.github.lizhangqu:coreprogress:1.0.2'
        ```

    - <a href="https://github.com/airbnb/lottie-android" target="_blank">*Lottie*</a> is a mobile library for Android and iOS that parses Adobe After Effects animations exported as json with Bodymovin and renders them natively on mobile!
        ```gradle
        implementation 'com.airbnb.android:lottie:5.2.0'
        ```

    - <a href="https://github.com/wajahatkarim3/EasyFlipViewPager" target="_blank">*EasyFlipViewPager*</a> : android library to create book & card flipping animations in ViewPager
        ```gradle
        implementation 'com.wajahatkarim:easyflipviewpager:2.0.1'
        ```

    - <a href="https://github.com/jsibbold/zoomage" target="_blank">*Zoomage*</a> : a simple pinch-to-zoom ImageView library for Android with an emphasis on a smooth and natural feel.
        ```gradle
        implementation 'com.jsibbold:zoomage:1.3.1'
        ```