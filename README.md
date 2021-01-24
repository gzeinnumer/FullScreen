# FullScreen

|![](https://github.com/gzeinnumer/FullScreen/blob/master/preview/preview1.jpg)|![](https://github.com/gzeinnumer/FullScreen/blob/master/preview/preview2.jpg)|![](https://github.com/gzeinnumer/FullScreen/blob/master/preview/preview3.jpg)|![](https://github.com/gzeinnumer/FullScreen/blob/master/preview/preview4.jpg)|
|---|---|
|Samsung A51(Status Bar Hide)|Samsung A51(Status Bar Show)| Vivo 1719(Status Bar Show)| Vivo 1719(Status Bar Hide)|

- `Manifest.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest >

    <application >
        <activity android:name=".MainActivity"
            android:theme="@style/Theme.AppCompat.Light.NoActionBar">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

- `style.xml`
```xml
<style name="Theme.AppCompat.Light.NoActionBar">
    <item name="windowActionBar">false</item>
    <item name="windowNoTitle">true</item>
</style>
```

- `MainActivity.java`
```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        //add this kode
        requestWindowFeature(Window.FEATURE_NO_TITLE);
        getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN,
                WindowManager.LayoutParams.FLAG_FULLSCREEN);

        setContentView(R.layout.activity_main);
    }
}
```

- `activity_main.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="FullScreen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</LinearLayout>
```

---

```
Copyright 2021 M. Fadli Zein
```