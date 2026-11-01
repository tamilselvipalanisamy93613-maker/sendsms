
# Ex.No:6 Design an android application Send SMS using Intent.


## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application Send SMS using Intent.
Developed by: TAMILSELVI P
Registeration Number :212225040460
*/
```
## activity_Main.xml
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">


    <EditText
        android:id="@+id/phoneNumber"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="8726534726"
        android:inputType="phone"/>

    <EditText
        android:id="@+id/message"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Hello"
        android:inputType="textMultiLine"/>

    <Button
        android:id="@+id/sendButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send SMS"/>


</LinearLayout>
```
## MainActivity.java
```
package com.example.sendsms;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {


    EditText phoneNumber, message;
    Button sendButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        phoneNumber = findViewById(R.id.phoneNumber);
        message = findViewById(R.id.message);
        sendButton = findViewById(R.id.sendButton);

        sendButton.setOnClickListener(v -> {

            String number = phoneNumber.getText().toString();
            String msg = message.getText().toString();

            Intent intent = new Intent(Intent.ACTION_SENDTO);
            intent.setData(Uri.parse("smsto:" + number));
            intent.putExtra("sms_body", msg);

            startActivity(intent);
        });
    }


}
```


## OUTPUT
<img width="1917" height="1078" alt="Screenshot 2026-11-01 190332" src="https://github.com/user-attachments/assets/797817f6-50b4-4933-a3cc-9a75b6b3c1ed" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 190435" src="https://github.com/user-attachments/assets/9925cfcc-c2a9-441c-93a3-800897269133" />

<img width="1917" height="1076" alt="Screenshot 2026-11-01 190543" src="https://github.com/user-attachments/assets/1f066231-9e7d-4091-a91a-1f4fe6c8bd73" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 190557" src="https://github.com/user-attachments/assets/14c1eeab-582f-42bb-b837-589a074b6cd1" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 190755" src="https://github.com/user-attachments/assets/3585a91e-fd3c-4f67-8e1d-1bb7951fca77" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 191105" src="https://github.com/user-attachments/assets/7c321f52-61ce-496e-a114-322c88b0368d" />


## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.
