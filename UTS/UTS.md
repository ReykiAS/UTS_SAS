# UTS

**Gede Reyki Astika   1202190052 **

------

### Soal

### 1.Download ISO Installer windows server 2022 

a. https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022

### 2. Buat sebuah dokumentasi instalasi di github yang berisi

a. Instalasi windows server 2022

b. Instalasi Active Directory Domain Services

c. Instalasi DNS server

d. Instalasi Net Framework 3.5

e. Promote Server to a Domain Controller



------

### Step by Step



1. Download file iso windows server di link yang telah diberikan 

    https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022

   ![1_0_Instalasi](assets/1_0_Instalasi.PNG)

   2. Install Windows Server

      

      ![1_1_Instalasi](assets/1_1_Instalasi.PNG)

      install windows server di oracle vm dengan create virtual machine

      ![1_2_Masukan FIle](assets/1_2_Masukan_FIle.PNG)

      Masukan file iso yang telah didownload di link yang telah diberikan

      ![1_3_Proses  Instalasi](assets/1_3_Proses_Instalasi.PNG)

      Memulai proses instalasi windows server 2022

      

      ![1_4_Memilih Versi](assets/1_4_Memilih_Versi.PNG)

      Memilih versi windows server yang digunakan yang dimana pada instalasi kali ini menggunakan windows server 2022 standard evaluation

      ![1_5_Memilih Operating System](assets/1_5_Memilih_Operating_System.PNG)

      

      untuk penginstalan nya disini saya memilih untuk custom: install server operating system only

      ![1_6_Pembagian Versi](assets/1_6_Pembagian_Versi.PNG)

      pembagian partisi yang digunakan yang dimana disini menggunakan 20 gb dengan satu drive saja

      

      ![1_7_install](assets/1_7_install.PNG)

      memulai proses penginstalan windows server 2022

      ![1_8_passwd](assets/1_8_passwd.PNG)

      Masukan password yang diinginkan jangn lupa untuk forma password harus berisi : huruf kapital, huruf kecil dan angka

      ![1_8_Done](assets/1_8_Done.PNG)

      Tampilan ui windows server 2022

      

------

### Menginstall roles dan features



![2_1_Konfigurasi](assets/2_1_Konfigurasi.PNG)

Mengatur adapter network yang dimana dari nat menjadi bridge adapter

![2_2_Konfigurasi ip](assets/2_2_Konfigurasi_ip.PNG)

Mengubah ip dari dhcp menjadi static yang dimana saya menggunakan ip 192.168.43.12, untuk cara mengubah ip dengan cara, menuju network and internet lalu ke network connection masuk kedalam ethernet status lalu properties, cari internet protocol version 4.

![2_3_Konfigurasi berhasil](assets/2_3_Konfigurasi_berhasil.PNG)

ip berhasil berubah, untuk mengcek ip bisa melalui, win + r lalu ketik cmd dan ketik ipconfig

![2_4_Menambahkan role](assets/2_4_Menambahkan_role.PNG)

menambahkan roles dan features dengan mengklik add roles and features yang dimana disini kita akan menginstall win Active Directory Domain Services, DNS server dan Net Framework 3.5

![2_5_Memilih_roles_ type](assets/2_5_Memilih_roles_ type.PNG)

untuk type yang digunakan ialah role based or feature based installation

![2_6_Server_Selection](assets/2_6_Server_Selection.PNG)

Untuk server pool yang digunakan ialah windows server yang kita install 

![2_7_Server_Roles](assets/2_7_Server_Roles.PNG)

di menu server roles kita akan memilih roles, active directory domain services dan dns server

![2_8_Server_Features](assets/2_8_Server_Features.PNG)

di menu features kita memilih net framework 3.5 features

![2_9_Confirmation](assets/2_9_Confirmation.PNG)

setelah mengisi semua roles yang dibutuhkan kita langsung ke menu confirmation, yang dimana kita jangan langsung menekan install akan tetapi, klik specify an alternate source path yang dimana disini kita akan mengisi path

![2_10_Sources_path](assets/2_10_Sources_path.PNG)

tampilan menu specify alternate source path, di sini kita akan mengisi lokasi path yang diinginkan

![2_13_Sources_sxs](assets/2_13_Sources_sxs.PNG)

untuk lokasi path itu sendiri terdapat pada file iso yang dimana itu berlokasikan di : D:\sources\sxs

![2_14_copy_sources_sxs](assets/2_14_copy_sources_sxs.PNG)

copy file lokasi path yang telah dicari tadi yaitu : D:\sources\sxs

![2_15_Proses_Instalasi](assets/2_15_Proses_Instalasi.PNG)

lalu sekarang jalankan instalasi dan tunggu hingga instalasi selesai

------



### Promote Domain

![3_1_Promote Domain](assets/3_1_Promote_Domain.PNG)

Jalankan promote server yang dimana akan terdapat tanda bendera berwarna kuning, setelah itu kita mengklik promote this server

![3_2_add_new_forest](assets/3_2_add_new_forest.PNG)

langkah pertama menambahkan forest yang dimana disini kita menambahkan root domain name kita

![3_3_Domian_Controll](assets/3_3_Domian_Controll.PNG)

setelah itu  memasukan password yang telah di set pada saat instalasi windows server

![3_4_install](assets/3_4_install.PNG)

Setelah itu mulai proses instalasi, yang dimana disini kita akan diberitahukan kita telah mengisi apa saja

![3_5_promote_server_berhasil](assets/3_5_promote_server_berhasil.PNG)

untuk melihat apakah promote server telah berhasil atau tidak kita dapat melihat di, tools -> active directory Users and Computers

![3_6_ping_vm_local](assets/3_6_ping_vm_local.PNG)

Ping vm.local, yang dimana menandakan promote telah berhasil dilakukan





