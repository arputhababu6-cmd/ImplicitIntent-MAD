# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1. Start the project: Create a new Android project in Android Studio.

2. Design the UI: In activity_main.xml, add an EditText (to accept the URL input) and a Button (to trigger the navigation).

3. Initialize components: In MainActivity.java, map the EditText and Button variables to their respective XML IDs using findViewById().

4. Set click listener: Attach an OnClickListener to the button to listen for user click events.

5. Get input: Inside the onClick method, extract the text entered in the EditText and convert it to a string.

6. Create implicit intent: Instantiate an Intent with the action Intent.ACTION_VIEW and pass the parsed URL string using Uri.parse().

7. Start activity: Call startActivity(intent) to trigger the OS to open the webpage in an available web browser.

8. Stop: Run and test the application.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:
Registeration Number :
*/
```
Main Activity:
```
package com.example.implicitintent;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = findViewById(R.id.editText);

        button.setOnClickListener(
```
Activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="search"
        android:text="Search"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.588"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText"
        app:layout_constraintVertical_bias="0.484" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="157dp"
        android:layout_height="28dp"
        android:text="implict intent"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/editText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.598"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.625" />


</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

<img width="1918" height="1017" alt="image" src="https://github.com/user-attachments/assets/8718ef67-9589-4b42-9839-bc9c32f9ad50" />

<img width="1918" height="1013" alt="image" src="https://github.com/user-attachments/assets/26ee5420-172b-42b2-a37b-b0194abc7f4b" />

<img width="1918" height="1020" alt="image" src="https://github.com/user-attachments/assets/2fda7756-1763-4e79-9724-58c0f6b2b018" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


