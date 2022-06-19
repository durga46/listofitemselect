# <p align="center"> Ex.No: 8 Build a program to show five checkboxes and toast selected checkboxes.</p>

## AIM:
To create a list using checkbox to display selected checkbox item using Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Arctic Fox)

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as "listofitemselect" and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the list using checkbox in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```python
/*
Program to display "check list item”.
Developed by        : DurgaDevi P
Registration Number : 212220230015
*/
```
## MainActivity.java
```python
package com.example.checkboxes;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    private CheckBox chkCSE, chkEEE, chkECE, chkMECH, chkCIVIL, chkAIDS, chkAIML, chkEIE, chkBME;

    @Override
    public void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        chkCSE = findViewById(R.id.cse);
        chkEEE = findViewById(R.id.eee);
        chkECE = findViewById(R.id.ece);
        chkMECH = findViewById(R.id.mech);
        chkCIVIL = findViewById(R.id.civil);
        chkAIDS = findViewById(R.id.aids);
        chkAIML = findViewById(R.id.aiml);
        chkEIE = findViewById(R.id.eie);
        chkBME = findViewById(R.id.bme);
    }

    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkCSE.isChecked())
            selected += "CSE";

        if(chkEEE.isChecked())
            selected += "\nEEE";

        if(chkECE.isChecked())
            selected += "\nECE";

        if(chkMECH.isChecked())
            selected += "\nMECH";

        if(chkCIVIL.isChecked())
            selected += "\nCIVIL";

        if(chkAIDS.isChecked())
            selected += "AIDS";

        if(chkAIML.isChecked())
            selected += "AIML";

        if(chkEIE.isChecked())
            selected += "EIE";

        if(chkBME.isChecked())
            selected += "BME";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```
## activity_main.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/linearLayout"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent">

    <TextView
        android:id="@+id/textView"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="10dp"
        android:layout_marginLeft="10dp"
        android:layout_marginEnd="10dp"
        android:layout_marginRight="10dp"
        android:layout_marginBottom="10dp"
        android:gravity="center"
        android:text="Choose The Course"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/cse"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="@+id/cse" />

    <CheckBox
        android:id="@+id/cse"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="40dp"
        android:layout_marginLeft="40dp"
        android:layout_marginTop="90dp"
        android:text="CSE"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <CheckBox
        android:id="@+id/eee"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="EEE"
        app:layout_constraintStart_toStartOf="@+id/cse"
        app:layout_constraintTop_toBottomOf="@+id/cse" />

    <CheckBox
        android:id="@+id/ece"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="ECE"
        app:layout_constraintStart_toStartOf="@+id/eee"
        app:layout_constraintTop_toBottomOf="@+id/eee" />

    <CheckBox
        android:id="@+id/mech"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="MECH"
        app:layout_constraintStart_toStartOf="@+id/ece"
        app:layout_constraintTop_toBottomOf="@+id/ece" />

    <CheckBox
        android:id="@+id/civil"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CIVIL"
        app:layout_constraintStart_toStartOf="@+id/mech"
        app:layout_constraintTop_toBottomOf="@+id/mech" />

    <CheckBox
        android:id="@+id/aids"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="AIDS"
        app:layout_constraintStart_toStartOf="@+id/civil"
        app:layout_constraintTop_toBottomOf="@+id/civil" />

    <CheckBox
        android:id="@+id/aiml"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="AIML"
        app:layout_constraintStart_toStartOf="@+id/aids"
        app:layout_constraintTop_toBottomOf="@+id/aids" />

    <CheckBox
        android:id="@+id/eie"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="EIE"
        app:layout_constraintStart_toStartOf="@+id/aiml"
        app:layout_constraintTop_toBottomOf="@+id/aiml" />

    <CheckBox
        android:id="@+id/bme"
        style="@style/TextAppearance.AppCompat.Headline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="BME"
        app:layout_constraintStart_toStartOf="@+id/eie"
        app:layout_constraintTop_toBottomOf="@+id/eie" />

    <Button
        android:id="@+id/btnDisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="128dp"
        android:layout_marginTop="88dp"
        android:background="@color/black"
        android:onClick="showSelected"
        android:text="Display"
        android:textColor="@color/white"
        app:layout_constraintStart_toStartOf="@+id/bme"
        app:layout_constraintTop_toBottomOf="@+id/bme" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT:
![o1](https://user-images.githubusercontent.com/75235704/173041855-3c199acb-1c5e-4623-9bc7-ccc5c894de63.png)
![o2](https://user-images.githubusercontent.com/75235704/173041868-41a6480f-5e9e-4d05-8015-2b1d2c4aa1f7.png)



## RESULT:
Thus a Simple Android Application to create a list using checkbox to display selected checkbox using Android Studio is developed and executed successfully.
