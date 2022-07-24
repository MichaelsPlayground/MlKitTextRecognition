# CameraX and ML Kit for text recognition example

Uses a rectangle view for cropping the image from cameraX before running the text recognition 

working


AndroidManifest:
```plaintext
    <uses-feature android:name="android.hardware.camera.any" />
    <uses-permission android:name="android.permission.CAMERA" />
    
    <application>
    ...
    <meta-data
      android:name="com.google.mlkit.vision.DEPENDENCIES"
      android:value="ocr" />
  <!-- To use multiple models: android:value="ocr,model2,model3" -->
    </application>
```

Gradle:
```plaintext
    //def camerax_version = "1.0.0-beta07"
    def camerax_version = "1.1.0"
    implementation "androidx.camera:camera-camera2:$camerax_version"
    implementation "androidx.camera:camera-lifecycle:$camerax_version"
    implementation "androidx.camera:camera-view:$camerax_version"   
    implementation 'androidx.exifinterface:exifinterface:1.3.3'
    // Text features
    implementation 'com.google.android.gms:play-services-mlkit-text-recognition:18.0.0'
```