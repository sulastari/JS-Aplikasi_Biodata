# JS-Aplikasi_Biodata
Tugas Akhir Pemrograman Perangkat Mobile

.............. ACTIVITY_MAIN ..............

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
