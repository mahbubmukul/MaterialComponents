# MaterialComponents
## 1. Depend on our library

* Add a single Gradle dependency to your app/module ```build.gradle``` file:

  ```implementation "com.google.android.material:material:1.0.0"```

## 2. New Namespace and AndroidX

If your app currently depends on the original Design Support Library, you can make use of the Refactor to AndroidX… option provided by Android Studio. Doing so will update your app's dependencies and code to use the newly packaged androidx and com.google.android.material libraries.

With Android Studio 3.2 and higher, you can quickly migrate an existing project to use AndroidX by selecting **Refactor > Migrate** to AndroidX from the menu bar.

If you don't want to switch over to the new androidx and com.google.android.material packages yet, you can use Material Components via the com.android.support:design:28.0.0 dependency.

## 3. Change your app theme to inherit from a Material Components theme

Update your app theme to inherit from one of these themes, e.g.:

  ```xml
  <style name="Theme.MyApp" parent="Theme.MaterialComponents.DayNight">
      <!-- ... -->
  </style> 
  ```

If you cannot change your theme to inherit from a Material Components theme, you can inherit from a Material Components Bridge theme.

  ```xml
  <style name="Theme.MyApp" parent="Theme.MaterialComponents.Light.Bridge">
      <!-- ... -->
  </style> 
  ```
  
  ## 4. Add a Material component to your app
  
  #### Implementing a text field via XML
  The default filled text field XML is defined as:

  ```xml
  <com.google.android.material.textfield.TextInputLayout
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="@string/textfield_label">

    <com.google.android.material.textfield.TextInputEditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
  </com.google.android.material.textfield.TextInputLayout>
  ```
  Note: If you are not using a theme that inherits from a Material Components theme, you will have to specify the text field  style as well, via style="@style/Widget.MaterialComponents.TextInputLayout.FilledBox"

  Other text field styles are also provided. For example, if you want an outlined text field in your layout, you can apply the Material Components outlined style to the text field in XML:

  ```xml
  <com.google.android.material.textfield.TextInputLayout
      style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="@string/textfield_label">

    <com.google.android.material.textfield.TextInputEditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
  </com.google.android.material.textfield.TextInputLayout>
  ```
