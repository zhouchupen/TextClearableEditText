# TextClearableEditText

Android自定义带标题和可清除功能的EditText

![](http://upload-images.jianshu.io/upload_images/2746415-8593855baacec45b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



## Installing

Users of your library will need add the jitpack.io repository:

```gradle
allprojects {
 repositories {
    jcenter()
    maven { url "https://jitpack.io" }
 }
}
```

and:

```gradle
dependencies {
    compile 'com.github.zhouchupen:TextClearableEditText:v1.0'
}
```

Note: do not add the jitpack.io repository under `buildscript` 

## Adding a sample app 

If you add a sample app to the same repo then your app needs to depend on the library. To do this in your app/build.gradle add a dependency in the form:

```gradle
dependencies {
    compile project(':library')
}
```

where 'library' is the name of your library module.

## Using

You may need this to use the edittext.  Put this into your xml file:
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <com.scnu.zhou.widget.TextClearableEditText
        android:id="@+id/et_user"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:title="用户名"
        app:hint="请输入用户名"
        app:lineColor="#97CC00"
        app:singleline="true"
        android:layout_marginTop="15dp">

    </com.scnu.zhou.widget.TextClearableEditText>

    <com.scnu.zhou.widget.TextClearableEditText
        android:id="@+id/et_password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:title="密码"
        app:hint="请输入密码"
        app:lineColor="#97CC00"
        app:singleline="true"
        app:password="true"
        android:layout_marginTop="15dp">

    </com.scnu.zhou.widget.TextClearableEditText>

</LinearLayout>
```
where ‘lineColor’ is the color of the underline, and you can set 'password' as true to make the input type of edittext 'password'.
