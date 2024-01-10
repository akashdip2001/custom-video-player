# freecad_app 


|🍭 [Downlod-app 🍭](https://www.mediafire.com/file/njc51t2ierhir85/akashdipmahapatraFreeCAD.apk/file) |🐥 [in app interface 🐥](https://akashdip2001.github.io/freecad_app/) |❌ [videos](https://engineering-aot.github.io/custom-video-player/freecad_exam.html) ❌|
|-------------------- |-------------------- |-------------------- |

![webapp dev (2)](https://github.com/akashdip2001/freecad_app/assets/81384987/beec1827-4afe-4394-9394-941db53c43db)
![webapp dev (3)](https://github.com/akashdip2001/freecad_app/assets/81384987/979c980e-77e1-432a-b69a-2da4e18f22ad)

# Android studio code

# activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <WebView
        android:id="@+id/webView"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</LinearLayout>
```
# MainActivity.java
```
package com.example.cadpro;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
import android.webkit.WebSettings;
import android.webkit.WebView;

public class MainActivity extends AppCompatActivity {
    private WebView webView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        webView = findViewById(R.id.webView);
        WebSettings webSettings = webView.getSettings();
        webSettings.setJavaScriptEnabled(true); // Enable JavaScript if your site requires it

        // Load the URL into the WebView
        webView.loadUrl(getString(R.string.webview_url));
    }
}
```
# AndroidManifes.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.CADPro"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        tools:targetApi="31">

        <activity
            android:name=".MainActivity"
            android:screenOrientation="portrait"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

    </application>

</manifest>
```
# Strings.xml
```
<resources>
    <string name="app_name">CAD pro</string>
    <string name="webview_url">https://akashdip2001.github.io/freecad_app/</string>
</resources>
```

![webapp dev (1)](https://github.com/akashdip2001/freecad_app/assets/81384987/ce9f6d8e-965e-4aed-970e-28d0fa2babb7)
![webapp dev (4)](https://github.com/akashdip2001/freecad_app/assets/81384987/2054e341-77be-413b-aa33-58fa735e574e)
![webapp dev (5)](https://github.com/akashdip2001/freecad_app/assets/81384987/7dd4bb0e-4821-4e26-be0b-a5034561bdcb)

# Blur complet page - Desktop mode - Except "Action Button"
```
    <script>
        // Function to check if the user is on a desktop device
        function isDesktop() {
            return window.innerWidth > 768; // Adjust the width based on your design
        }

        // Check if the user is on a desktop and apply backdrop blur with increased intensity if true
        window.addEventListener('DOMContentLoaded', function () {
            if (isDesktop()) {
                document.body.style.filter = "blur(10px)"; // Increase the blur intensity by adjusting the value (e.g., 10px)
                document.body.style.pointerEvents = "none"; // Disable pointer events on the body

                // Enable pointer events on the Subscribe button
                var subscribeButton = document.querySelector('.Action-button a');
                if (subscribeButton) {
                    subscribeButton.style.pointerEvents = "auto";
                }
            }
        });
    </script>
```

# Disable Right Click
```
 <script>
        // Function to disable right-click context menu
        function disableRightClick(event) {
            event.preventDefault();
        }

        // Attach the disableRightClick function to the contextmenu event
        window.addEventListener('contextmenu', disableRightClick);
    </script>
```

# Automatic redirect another site
```
<script>
        // Function to check if the user is on a desktop device
        function isDesktop() {
            return window.innerWidth > 768; // Adjust the width based on your design
        }

        // Function to redirect to another page
        function redirectToAnotherPage() {
            window.location.href = 'https://akashdip2001.github.io/404/';
        }

        // Check if the user is on a desktop and redirect if true
        window.addEventListener('DOMContentLoaded', function () {
            if (isDesktop()) {
                redirectToAnotherPage();
            }
        });
    </script>
```

![akashdip Mahapatra 4](https://github.com/akashdip2001/freecad_app/assets/81384987/9c663d1a-3a53-4d47-bdd8-a933bc26001d)
