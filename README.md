# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as ImplicitIntent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.
```



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: R.hema jai suriya 
Registeration Number : 212221040054
*/
```

#activitymain.xml

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:autofillHints="enterlink"
        android:id="@+id/editTextText"
        android:layout_width="290dp"
        android:layout_height="48dp"
        android:hint="@string/hint_web"
        android:inputType="text"
        android:textAlignment="center"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.495"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.935" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="324dp"
        android:text="@string/search_btn"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

#activitymain.java

```
package com.example.implicitintent;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.EditText;
import android.widget.Button;
import android.net.Uri;
import android.content.Intent;
import android.view.View;

public class MainActivity extends AppCompatActivity {
    EditText editText;
    Button button;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }

        });
    }
}
```

## OUTPUT
![impicit](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/41a89d39-bc31-422f-81bf-4e5659235857)
![afcf2c77-042c-4f53-86dc-4ec26244aced](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/d20763d4-0311-47cf-84ec-b59e9e00f96c)
![446547ce-28f6-41f0-aa63-d843e40de413](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/95dce8ec-d489-4351-954a-70b5b81aa4b1)












## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


