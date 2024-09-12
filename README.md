# PRM231
DEMO-CODE-SRC 13-09-2024



# 1. MainActivity.java
- Open MainActivity.java on your new project and replace  code inside exclude package name  by below code

```java
import android.content.Intent;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import androidx.appcompat.app.AppCompatActivity;


public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.e("onCreate ------ ", "MainActivity: onCreate()");
    }

    @Override
    protected void onStart() {
        super.onStart();
        Log.e("onStart ------ ","MainActivity: onStart()");
    }


    @Override
    protected void onResume() {
        super.onResume();
        Log.e("onResume ------ ","MainActivity: onResume()");
    }


    @Override
    protected void onPause() {
        super.onPause();
        Log.e("onPause ------ ","MainActivity: onPause()");
    }


    @Override
    protected void onStop() {
        super.onStop();
        Log.e("onStop ------ ","MainActivity: onStop()");
    }


    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.e("onDestroy ------ ","MainActivity: onDestroy()");
    }


    @Override
    protected void onRestart() {
        super.onRestart();
        Log.e("onRestart ------ ","MainActivity: onRestart()");

    }

    public void switchActivity(View view){
        Intent intent = new Intent(MainActivity.this, AnotherActivity.class);
        startActivity(intent);
    }
}

```

# 2. AnotherActivity.java
- Create a new activity name AnotherActivity
- Open AnotherActivity.java  replace  code inside exclude package name by below code

```java 
public class AnotherActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_another);
        Log.e("onCreate ------ ", "AnotherActivity: onCreate()");
    }

    @Override
    protected void onStart() {
        super.onStart();
        Log.e("onStart ------ ", "AnotherActivity: onStart()");
    }


    @Override
    protected void onResume() {
        super.onResume();
        Log.e("onResume ------ ", "AnotherActivity: onResume()");
    }


    @Override
    protected void onPause() {
        super.onPause();
        Log.e("onPause ------ ", "AnotherActivity: onPause()");
    }


    @Override
    protected void onStop() {
        super.onStop();
        Log.e("onStop ------ ", "AnotherActivity: onStop()");
    }


    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.e("onDestroy ------ ", "AnotherActivity: onDestroy()");
    }


    @Override
    protected void onRestart() {
        super.onRestart();
        Log.e("onRestart ------ ", "AnotherActivity: onRestart()");

    }

    public void switchToMain(View view){
        Intent intent = new Intent( AnotherActivity.this    ,MainActivity.class);
        startActivity(intent);
    }
}
```

# 3. activity_main.xml
- Open activity_main.xml and insert below code
```xml
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:id="@+id/activity_main"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:paddingBottom="10dp"
        android:paddingLeft="10dp"
        android:paddingRight="10dp"
        android:paddingTop="10dp"
        tools:context="com.example.android.testapp.MainActivity"
        android:orientation="vertical">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="center_horizontal"
            android:text="Main Activity"
            android:textSize="40sp" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:onClick="switchActivity"
            android:text="Switch to another activity" />
    </LinearLayout>
```
# 4. activity_another.xml
- Open activity_another.xml and insert below code
```xml
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:orientation="vertical"
        android:id="@+id/activity_another"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:paddingBottom="10dp"
        android:paddingLeft="10dp"
        android:paddingRight="10dp"
        android:paddingTop="10dp"
        >

        <TextView
            android:gravity="center_horizontal"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Second Activity"
            android:textSize="40sp"/>
        <Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:onClick="switchToMain"
            android:text="Back to main activity" />
    </LinearLayout>
```


