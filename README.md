# JS-Aplikasi_Biodata
Tugas Akhir Pemrograman Perangkat Mobile

.............. SCRIPT CODE ACTIVITY_MAIN ..............

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:padding="20dp"
    android:orientation="vertical">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"/>

    <EditText
        android:id="@+id/edt_namapanjang"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Nama Panjang"/>

    <EditText
        android:id="@+id/edt_namapanggilan"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Nama Panggilan" />

    <Spinner
        android:id="@+id/spn_jkelamin"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginVertical="10dp"></Spinner>

    <Space
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/edt_tempatlahir"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Tempat  Lahir" />

    <Button
        android:id="@+id/btn_tgllahir"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="TANGGAL LAHIR" />

    <EditText
        android:id="@+id/edt_alamat"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Alamat" />

    <EditText
        android:id="@+id/edt_hobi"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Hobi" />

    <EditText
        android:id="@+id/edt_pekerjaan"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Pekerjaan" />

    <Button
        android:id="@+id/btn_proses"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="PROSES" />

    <TextView
        android:id="@+id/txt_kalimatpengenalan"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Kalimat Pengenalan Diri"/>

</LinearLayout>





............... Script Code MainActivity ...............



package com.sulas.Biodata;

import androidx.appcompat.app.AppCompatActivity;

import android.app.DatePickerDialog;

import android.os.Bundle;

import android.view.View;

import android.widget.ArrayAdapter;

import android.widget.Button;

import android.widget.DatePicker;

import android.widget.EditText;

import android.widget.Spinner;

import android.widget.TextView;

import java.util.ArrayList;

import java.util.Calendar;

import java.util.List;

public class MainActivity extends AppCompatActivity {

    EditText namapanjang,namapanggilan,tempatlahir,alamat,hobi,pekerjaan;
    Spinner jkelamin;
    Button tgllahir,proses;
    TextView kalimatpengenalan;
    private int mTahun;
    private int mBulan;
    private int mHari;
    
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        namapanjang = (EditText)findViewById(R.id.edt_namapanjang);
        namapanggilan = (EditText)findViewById(R.id.edt_namapanggilan);
        tempatlahir = (EditText)findViewById(R.id.edt_tempatlahir);
        alamat = (EditText)findViewById(R.id.edt_alamat);
        hobi = (EditText)findViewById(R.id.edt_hobi);
        pekerjaan = (EditText)findViewById(R.id.edt_pekerjaan);

        jkelamin = (Spinner) findViewById(R.id.spn_jkelamin);

        tgllahir = (Button) findViewById(R.id.btn_tgllahir);
        proses = (Button) findViewById(R.id.btn_proses);

        kalimatpengenalan = (TextView) findViewById(R.id.txt_kalimatpengenalan);

        List<String> listKelamin = new ArrayList<String>();
        listKelamin.add("Laki - Laki");
        listKelamin.add("Perempuan");

        ArrayAdapter<String> adapter = new ArrayAdapter<String>(this, android.R.layout.simple_spinner_item, listKelamin);
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
        jkelamin.setAdapter(adapter);


        tgllahir.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Calendar cal = Calendar.getInstance();
                mTahun = cal.get(Calendar.YEAR);
                mBulan = cal.get(Calendar.MONTH);
                mHari = cal.get(Calendar.DAY_OF_MONTH);

                DatePickerDialog mDateDialog = new DatePickerDialog(MainActivity.this, new DatePickerDialog.OnDateSetListener(){
                @Override
                public void onDateSet(DatePicker view, int year, int month, int dayOfMonth) {
                    tgllahir.setText(String.valueOf(dayOfMonth)+"_"+String.valueOf(month)+"_"+String.valueOf(year));
                }
                },mTahun, mBulan, mHari);
        mDateDialog.setTitle("Pilih Tanggal Lahir");
        mDateDialog.show();
            }
        });


                 proses.setOnClickListener(new View.OnClickListener() {
                     @Override
                     public void onClick(View v) {

              kalimatpengenalan.setText("Hai nama saya adalah"+namapanjang.getText().toString()+",saya biasa dipanggil"+
              namapanggilan.getText().toString()+",saya lahir di "+tempatlahir.getText().toString()+","+tgllahir.getText().toString()+"," +
                      "alamat saya di "+alamat.getText().toString()+",hobi saya adalah "+hobi.getText().toString()+"," +
                      "dan pekerjaan saya adalah "+pekerjaan.getText().toString()+", Senang berkenalsan dengan kalian ...!!!");

          }
          } );


    }
    }
