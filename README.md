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
![image](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/008f4eaf-a538-4761-888a-627c05ca448b)
![image](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/86696d9b-ca8e-4a0d-a66b-e77cbd371875)
![image](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/763ad5d2-970b-4233-b940-2ede6f94e2e4)
![image](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/ce28a033-5f47-4dbd-9a50-55fa2f9fc228)
![image](https://github.com/Hemajaisuriya/ImplicitIntent-MAD/assets/147486496/3e428c5b-98d8-43fd-871c-9478cf766e0b)









## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


