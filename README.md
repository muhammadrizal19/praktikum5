# praktikum5
Buat program sederhana untuk menampilkan daftar nilai mahasiswa dengan ketentuan :

1. program dibuat menggunakan dictionary
2. tampilkan menu pilihan ( tambah data, ubah data, hapus data, tampilkan data, cari data)
3. nilai akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, uts : 35%, uas : 35%)
# Penjelasan Program: 
1. Fungsi hitung_nilai_akhir: Menghitung nilai akhir berdasarkan komponen tugas, UTS, dan UAS dengan bobot yang sudah ditentukan.
2. Fungsi tambah_data: Menambahkan data mahasiswa ke dalam dictionary.
3. Fungsi ubah_data: Mengubah data mahasiswa berdasarkan NIM yang dimasukkan.
4. Fungsi hapus_data: Menghapus data mahasiswa berdasarkan NIM yang dimasukkan.
5. Fungsi tampilkan_data: Menampilkan semua data mahasiswa yang tersimpan.
6. Fungsi cari_data: Mencari dan menampilkan data mahasiswa berdasarkan NIM.
# Penjelasan Setiap Menu
# 1. Menampilkan menu (Tambah Data)
1. Definisi Fungsi:

     def tambah_data(mahasiswa): mendefinisikan sebuah fungsi bernama tambah_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2. Input NIM:

    nim = input("Masukkan NIM mahasiswa: ") meminta pengguna untuk memasukkan NIM (Nomor Induk Mahasiswa) dari mahasiswa yang akan ditambahkan. Nilai ini disimpan dalam variabel nim.
    
4. Input Nama:

   nama = input("Masukkan nama mahasiswa: ") meminta pengguna untuk memasukkan nama mahasiswa. Nilai ini disimpan dalam variabel nama.

5. Input Nilai Tugas, UTS, dan UAS:

   tugas = float(input("Masukkan nilai tugas: ")) meminta pengguna untuk memasukkan nilai tugas dan mengkonversinya menjadi tipe data float agar dapat melakukan perhitungan desimal. uts = float(input("Masukkan nilai UTS: ")) dan uas = float(input("Masukkan nilai UAS: ")) melakukan hal yang sama untuk nilai UTS dan UAS.

6. Menghitung Nilai Akhir:

  nilai_akhir = hitung_nilai_akhir(tugas, uts, uas) memanggil fungsi hitung_nilai_akhir yang telah didefinisikan sebelumnya, dengan parameter nilai tugas, UTS, dan UAS. Fungsi ini akan menghitung nilai akhir berdasarkan bobot yang telah ditentukan (tugas: 30%, UTS: 35%, UAS: 35%).

7. Menambahkan Data ke Dictionary:

  mahasiswa[nim] = {'nama': nama, 'tugas': tugas, 'uts': uts, 'uas': uas, 'nilai_akhir': nilai_akhir} menambahkan data mahasiswa ke dalam dictionary mahasiswa dengan menggunakan NIM sebagai kunci. Nilai dari kunci ini adalah sebuah dictionary yang berisi nama, nilai tugas, UTS, UAS, dan nilai akhir.

8. Pesan Konfirmasi:

 print("Data mahasiswa berhasil ditambahkan.") menampilkan pesan konfirmasi kepada pengguna bahwa data mahasiswa telah berhasil ditambahkan.

# 2. Menampilkan menu (Ubah Data)

1. Definisi Fungsi:

  def ubah_data(mahasiswa): mendefinisikan sebuah fungsi bernama ubah_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa. 

2. Input NIM:
 
 nim = input("Masukkan NIM mahasiswa yang ingin diubah: ") meminta pengguna untuk memasukkan NIM (Nomor Induk Mahasiswa) dari mahasiswa yang datanya ingin diubah. Nilai ini disimpan dalam variabel nim.

3. Pengecekan NIM:

if nim in mahasiswa: memeriksa apakah NIM yang dimasukkan oleh pengguna ada dalam dictionary mahasiswa. Jika NIM tersebut ada, program akan melanjutkan ke langkah berikutnya. Jika tidak, program akan menampilkan pesan bahwa NIM tidak ditemukan.

4. Input Data Baru:

Jika NIM ditemukan, program akan meminta pengguna untuk memasukkan data baru: nama = input("Masukkan nama mahasiswa baru: ") untuk memasukkan nama baru. tugas = float(input("Masukkan nilai tugas baru: ")) untuk memasukkan nilai tugas baru, dan mengkonversinya menjadi tipe data float. uts = float(input("Masukkan nilai UTS baru: ")) untuk memasukkan nilai UTS baru. uas = float(input("Masukkan nilai UAS baru: ")) untuk memasukkan nilai UAS baru.

5.Menghitung Nilai Akhir:

 nilai_akhir = hitung_nilai_akhir(tugas, uts, uas) memanggil fungsi hitung_nilai_akhir, yang menghitung nilai akhir berdasarkan nilai tugas, UTS, dan UAS yang baru dimasukkan. Hasil perhitungan disimpan dalam variabel nilai_akhir.

6. Memperbarui Data di Dictionary:

 mahasiswa[nim] = {'nama': nama, 'tugas': tugas, 'uts': uts, 'uas': uas, 'nilai_akhir': nilai_akhir} mengupdate data mahasiswa yang ada di dalam dictionary mahasiswa dengan nilai-nilai baru yang telah dimasukkan oleh pengguna. Data baru disimpan dengan menggunakan NIM sebagai kunci.

7. Pesan Konfirmasi:

print("Data mahasiswa berhasil diubah.") menampilkan pesan konfirmasi kepada pengguna bahwa data mahasiswa telah berhasil diubah.

8. Pesan NIM Tidak Ditemukan:
 
Jika NIM yang dimasukkan tidak ditemukan dalam dictionary mahasiswa, maka program akan mengeksekusi bagian else dan menampilkan pesan print("NIM tidak ditemukan.").

# 3. Menampilkan menu (Hapus Data)

1. Definisi Fungsi:

def hapus_data(mahasiswa): mendefinisikan sebuah fungsi bernama hapus_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2.Input NIM:

nim = input("Masukkan NIM mahasiswa yang ingin dihapus: ") meminta pengguna untuk memasukkan NIM (Nomor Induk Mahasiswa) dari mahasiswa yang datanya ingin dihapus. Nilai ini disimpan dalam variabel nim.

3. Pengecekan NIM:

if nim in mahasiswa: memeriksa apakah NIM yang dimasukkan oleh pengguna ada dalam dictionary mahasiswa. Jika NIM tersebut ada, program akan melanjutkan ke langkah berikutnya. Jika tidak, program akan menampilkan pesan bahwa NIM tidak ditemukan.

4. Menghapus Data:

Jika NIM ditemukan, del mahasiswa[nim] akan menghapus entri yang terkait dengan NIM tersebut dari dictionary mahasiswa. Fungsi del digunakan untuk menghapus item dari dictionary berdasarkan kunci (dalam hal ini, NIM).

5. Pesan Konfirmasi:

print("Data mahasiswa berhasil dihapus.") menampilkan pesan konfirmasi kepada pengguna bahwa data mahasiswa telah berhasil dihapus.

6. Pesan NIM Tidak Ditemukan:

Jika NIM yang dimasukkan tidak ditemukan dalam dictionary mahasiswa, maka program akan mengeksekusi bagian else dan menampilkan pesan print("NIM tidak ditemukan.").

# 4. Menampilkan menu (Tampilkan Data)

1. Definisi Fungsi:

def tampilkan_data(mahasiswa): mendefinisikan sebuah fungsi bernama tampilkan_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2. Pengecekan Data Kosong:

if not mahasiswa: memeriksa apakah dictionary mahasiswa kosong. Jika kosong, maka program akan menampilkan pesan bahwa tidak ada data mahasiswa yang tersedia.

3. Menampilkan Data:

Jika ada data mahasiswa, program akan menampilkan pesan "Data Mahasiswa:" sebagai header. for nim, data in mahasiswa.items(): melakukan iterasi melalui setiap item dalam dictionary mahasiswa. nim adalah kunci (NIM mahasiswa), dan data adalah nilai (dictionary yang berisi informasi mahasiswa).

4. Menampilkan Informasi Mahasiswa:

Di dalam loop, program akan mencetak informasi mahasiswa dengan format yang jelas: print(f"NIM: {nim}") menampilkan NIM mahasiswa. print(f"Nama: {data['nama']}") menampilkan nama mahasiswa. print(f"Nilai Tugas: {data['tugas']}") menampilkan nilai tugas. print(f"Nilai UTS: {data['uts']}") menampilkan nilai UTS. print(f"Nilai UAS: {data['uas']}") menampilkan nilai UAS. print(f"Nilai Akhir: {data['nilai_akhir']}") menampilkan nilai akhir yang telah dihitung.

# 5. Menampilkan menu (Cari Data)

1. Definisi Fungsi:

def cari_data(mahasiswa): mendefinisikan sebuah fungsi bernama cari_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2. Input NIM:

nim = input("Masukkan NIM mahasiswa yang ingin dicari: ") meminta pengguna untuk memasukkan NIM (Nomor Induk Mahasiswa) dari mahasiswa yang datanya ingin dicari. Nilai ini disimpan dalam variabel nim.

3. Pengecekan NIM:

if nim in mahasiswa: memeriksa apakah NIM yang dimasukkan oleh pengguna ada dalam dictionary mahasiswa. Jika NIM tersebut ada, program akan melanjutkan untuk menampilkan data mahasiswa. Jika tidak, program akan menampilkan pesan bahwa NIM tidak ditemukan.

4. Menampilkan Data Mahasiswa:

Jika NIM ditemukan, program akan mengambil data mahasiswa terkait dengan NIM tersebut: data = mahasiswa[nim] menyimpan informasi mahasiswa dalam variabel data. Kemudian, program akan mencetak informasi mahasiswa dengan format yang jelas: print(f"NIM: {nim}") menampilkan NIM mahasiswa. print(f"Nama: {data['nama']}") menampilkan nama mahasiswa. print(f"Nilai Tugas: {data['tugas']}") menampilkan nilai tugas. print(f"Nilai UTS: {data['uts']}") menampilkan nilai UTS. print(f"Nilai UAS: {data['uas']}") menampilkan nilai UAS. print(f"Nilai Akhir: {data['nilai_akhir']}") menampilkan nilai akhir yang telah dihitung.

5. Pesan NIM Tidak Ditemukan:

Jika NIM yang dimasukkan tidak ditemukan dalam dictionary mahasiswa, maka program akan mengeksekusi bagian else dan menampilkan pesan print("NIM tidak ditemukan.").
# Flowchart
