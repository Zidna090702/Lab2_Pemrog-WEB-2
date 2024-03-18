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

![Screenshot 2024-03-18 235502](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/c751b4c3-8f43-4707-a134-4e120bc51b9d)

         <!DOCTYPE html>
         <html>
         <head>
             <title>Form Input</title>
         </head>
         <body>
         
         
         <h2>Form Input</h2>
         <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
             Nama: <input type="text" name="nama"><br>
             Tanggal Lahir: <input type="date" name="tanggal_lahir"><br>
             Pekerjaan:
             <select name="pekerjaan">
                 <option value="Pegawai Kantor">Pegawai Kantor</option>
                 <option value="Guru">Guru</option>
                 <option value="Dokter">Dokter</option>
             </select><br>
             <input type="submit" name="submit" value="Submit">
         </form>

   Outputnya

   ![output](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/d3a22057-207b-488b-832e-3bd813f3b3b1)

   2. Program untuk menghitung umur

         function hitungUmur($tanggal_lahir) {
                $tanggal_lahir = new DateTime($tanggal_lahir);
                $sekarang = new DateTime();
                $umur = $sekarang->diff($tanggal_lahir);
            
                $tahun = $umur->y;
                $bulan = $umur->m;
                $hari = $umur->d;
            
                return array($tahun, $bulan, $hari);
            }

3. membuat program untuk pekerjaan beserta gaji masing masing setiap pekerjaan nya

            // Array gaji berdasarkan pekerjaan
         $gaji_pekerjaan = array(
             "Pegawai Kantor" => 5000000,
             "Guru" => 6000000,
             "Dokter" => 15000000
         );

4. Program untuk menampilkan output

            if ($_SERVER["REQUEST_METHOD"] == "POST") {
             // Ambil nilai dari form
             $nama = $_POST["nama"];
             $tanggal_lahir = $_POST["tanggal_lahir"];
             $pekerjaan = $_POST["pekerjaan"];
         
             // Hitung umur
             list($tahun, $bulan, $hari) = hitungUmur($tanggal_lahir);
         
             // Tampilkan hasil
             echo "<h2>Hasil Input</h2>";
             echo "Nama: $nama <br>";
             echo "Tanggal Lahir: $tanggal_lahir <br>";
             echo "Umur: $tahun tahun, $bulan bulan, $hari hari <br>";
             echo "Pekerjaan: $pekerjaan <br>";
             echo "Gaji: Rp " . number_format($gaji_pekerjaan[$pekerjaan], 0, ',', '.') . "<br>";
         }

   5. Ini output untuk keseluruhan nya
  
      ![Screenshot 2024-03-19 000208](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/19d77668-114c-4b26-9552-d212677c298d)

      ![Screenshot 2024-03-19 000431](https://github.com/Zidna090702/Lab2_Pemrog-WEB-2/assets/115474076/3540f1ec-eba6-4f2e-a1ca-df3e519c71a8)


Sekian dan terimakasih :)

jangan lupa follow @zidna_zee

