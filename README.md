# TUGAS PEMROGRAMAN WEB 2 PERTEMUAN 3

Nama : Zidna Soleda Zulfa

NIM : 312210031

Kleas : TI.22.B1

# Pertanyaan dan Tugas

Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

Laporan Praktikum
Buatlah repository baru dengan nama Lab2Web.

# Kerjakan semua latihan yang diberikan sesuai urutannya.

1. Screenshot setiap perubahannya.

2. Buatlah file README.md dan tuliskan penjelasan dari setiap langkah praktikum beserta screenshotnya.

3. Commit hasilnya pada repository masing-masing.

4. Kirim URL repository pada e-learning ecampus

# Hasil

1. Membuat folder bernama lab2_php_dasar

   ![Screenshot 2024-03-17 230636](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/7b3061a1-3483-4d02-839c-cf27366e8299)

2. lalu buat file seperti di bawah ini

   ![Screenshot 2024-03-17 232824](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/403452e4-bc5d-41b8-ad58-bc21811f2429)

3. Ketikan source code

   A. Mendefinisikan sebuah form HTML dengan input untuk nama, tanggal lahir, dan pilihan pekerjaan.

         <!DOCTYPE html>
       <html>
       <head>
           <title>Form Input</title>
       </head>
       <body>
           <h2>Form Input</h2>
           <form method="post" action="">
               Nama: <input type="text" name="nama"><br><br>
               Tanggal Lahir: <input type="date" name="tanggal_lahir"><br><br>
               Pekerjaan:
               <select name="pekerjaan">
                   <option value="Programmer">Programmer</option>

   Output

   
                   <option value="Operator Produksi">Operator Produksi</option>
                   <option value="Admin">Admin</option>
               </select><br><br>
               <input type="submit" name="submit" value="Submit">
           </form>

