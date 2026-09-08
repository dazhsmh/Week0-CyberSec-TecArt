NIM: 260530911105  
Nama: Putu Satria Narayana Widiartha  
Divisi: Cyber Security

# Week0-CyberSec-TecArt  
Homework 00 bertujuan untuk memastikan setiap peserta telah memiliki lingkungan
kerja dan tools dasar yang diperlukan untuk mengikuti pembelajaran serta kompetisi
Cyber Security, khususnya Capture The Flag (CTF)

## Tools Umum  
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/tools-umum.png" width="300">

Instalasi tools umum yang telah diinstall:  
- WSL (Windows Subsytem for Linux) Distro Kali Linux  
- Git dan Github  
- Python

## Pengujian WSL  
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/create-readme.png" width="500">
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/nano-identitas.png" width="500">  

Pengujian WSL dilakukan sepenuhnya melalui Command Line Interface (CLI).
Langkah - langkah yang dilakukan:
1. Membuat sebuah folder dengan nama Week0-CyberSec-TecArt dengan command ```mkdir {nama_direktori}```.
2. Masuk ke dalam folder tersebut dengan command ```cd {direktori}```.
3. Membuat file baru dengan nama README.md dengan command ```nano {nama_file}```.
4. Lalu menuliskan informasi berikut pada file tersebut:  
- NIM
- Nama
- Divisi

## Pengujian Python  
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/create-py.png" width="500">
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/nano-py.png" width="500">  

Pengujian python dengan membuat program sederhana dilakukan dengan langkah - langkah berikut:
1. Membuat program menggunakan ```nano {nama program}``` dengan ekstensi file .py
2. Menuliskan kode program python
3. Menjalankan program menggunakan command ```python3 {nama_program.py}```

# Challenge  
Kerjakan challenge “Undo” pada platform CYLAB Academy:
https://learn.cylabacademy.org/library/766  
Dokumentasikan langkah-langkah penyelesaian challenge dalam write-up.  

## Pengerjaan Challenge Undo  
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/launch.png" width="500">  
<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/nc_soal.png" width="500">  

- Tekan tombol Launch Instance untuk memulai.  
- Hubungkan server soal dengan command ```nc {ip_address} {port}```  

Berikut 5 step yang muncul untuk menyelesaikan challenge ini.  

<img src="https://github.com/dazhsmh/Week0-CyberSec-TecArt/blob/main/challenge_undo.png" width="500">  

### --- Step 1 ---
```
Current flag: KTZvNHFycnE4LWZhMDFnQHplMHNmYTRlRy1nazNnLXRhMWZlcmlyRShTR1BicHZj
Hint: Base64 encoded the string.
Enter the Linux command to reverse it:
```
Untuk mendecode string yang didecode dengan base64, gunakan command ```base64 -d```  

### --- Step 2 ---
```
Current flag: )6o4qrrq8-fa01g@ze0sfa4eG-gk3g-ta1ferirE(SGPbpvc
Hint: Reversed the text.
Enter the Linux command to reverse it:
```
Untuk reverse sebuah text, gunakan command ```rev```  

### --- Step 3 ---
```
Current flag: cvpbPGS(Eriref1at-g3kg-Ge4afs0ez@g10af-8qrrq4o6)
Hint: Replaced underscores with dashes.
Enter the Linux command to reverse it:
```
Untuk mengganti seluruh dash menjadi underscore pada text, gunakan command ```tr "-" "_"```  

### --- Step 4 ---
```
Current flag: cvpbPGS(Eriref1at_g3kg_Ge4afs0ez@g10af_8qrrq4o6)
Hint: Replaced curly braces with parentheses.
Enter the Linux command to reverse it:
```
Untuk mengganti seluruh kurung menjadi kurawal pada text, gunakan command ```tr "()" "{}"```  

### --- Step 5 ---
```
Current flag: cvpbPGS{Eriref1at_g3kg_Ge4afs0ez@g10af_8qrrq4o6}
Hint: Applied ROT13 to letters.
Enter the Linux command to reverse it:
```
Untuk mendekripsi/mengenkripsi text dengan sandi ROT13, gunakan command ```tr "A-Za-z" "N-ZA-Mn-za-m"``` dimana huruf A-Z berubah menjadi N-Z dan A-M (Bergeser 13 huruf)  

Setelah mengerjakan seluruh step, kita akan mendapatkan sebuah flag. Copy flag tersebut lalu submit pada website untuk menyelesaikan challenge ini.  

Referensi:  
https://www.linuxsec.org/2018/09/base64-terminal.html  
https://www.geeksforgeeks.org/linux-unix/rev-command-in-linux-with-examples/  
https://www.tecmint.com/tr-command-examples-in-linux/  
https://medium.com/@marshal_demi/using-rot13-and-tr-command-e67c2bd607ed  

### Pengerjaan Challenge IntroToBurp (Kategori Web)  

Start instance lalu buka website target untuk mulai menganalisa. Saya menggunakan software Burp Suite yang telah terinstall di laptop saya untuk melakukan proses analisa. Website target berisikan form registrasi. Setelah mengisi form tersebut halaman dialihkan ke form otp.  
Setelah itu saya membuka Burp Suite lalu pergi ke dashboard Proxy dan menghidupkan mode Intercept. Gunakan web browser dari Burp Suite untuk menganalisa website target. Disaat saya mengisi lalu mengirim form otp, website mengirimkan sebuah request yang berisikan nilai otp dengan metode POST. Saya mencoba request tersebut di mode repeater lalu mencoba menghapus "otp=1234" untuk melihat responsenya. Flag berhasil di dapatkan dan challenge berhasil diselesaikan

### Pengerjaan Challenge Icibos Tekart 0 (Kategori Reverse Engineering dan Binary Exploitation)  
### Pengerjaan Challenge Icibos Tekart 1 (Kategori Reverse Engineering dan Binary Exploitation)  
