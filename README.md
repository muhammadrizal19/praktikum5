# Praktikum 5
Buat program sederhana untuk menampilkan daftar nilai mahasiswa dengan ketentuan :

1. program dibuat menggunakan dictionary
2. tampilkan menu pilihan ( tambah data, ubah data, hapus data, tampilkan data, cari data)
3. nilai akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, uts : 35%, uas : 35%)
![Screenshot_20241124_235423_Chrome](https://github.com/user-attachments/assets/e615ab42-2a93-4ae1-bbee-963b2720c3e2)
![Screenshot_20241124_235448_Chrome](https://github.com/user-attachments/assets/38afaf7b-4da7-4c4c-bddc-49d3783a69e2)
![Screenshot_20241124_235503_Chrome](https://github.com/user-attachments/assets/b9da0ff4-9438-468f-8bc7-e5c9bdfc4de1)
![Screenshot_20241124_235521_Chrome](https://github.com/user-attachments/assets/1cd31509-71f7-405b-8b86-17da42b8962b)
![Screenshot_20241124_235538_Chrome](https://github.com/user-attachments/assets/cdd3ffd0-4d1a-4901-a158-a32721d50438)
![Screenshot_20241124_235608_Chrome](https://github.com/user-attachments/assets/33d98f4b-35b8-454b-845e-9f260be82013)
![Screenshot_20241124_235633_Chrome](https://github.com/user-attachments/assets/583a13ba-758d-4587-a20b-78f1afa9327b)


# Penjelasan Program: 
1. Fungsi hitung_nilai_akhir: Menghitung nilai akhir berdasarkan komponen tugas, UTS, dan UAS dengan bobot yang sudah ditentukan.
2. Fungsi tambah_data: Menambahkan data mahasiswa ke dalam dictionary.
3. Fungsi ubah_data: Mengubah data mahasiswa berdasarkan NIM yang dimasukkan.
4. Fungsi hapus_data: Menghapus data mahasiswa berdasarkan NIM yang dimasukkan.
5. Fungsi tampilkan_data: Menampilkan semua data mahasiswa yang tersimpan.
6. Fungsi cari_data: Mencari dan menampilkan data mahasiswa berdasarkan NIM.
# Penjelasan Setiap Menu
# 1. Menampilkan menu (Tambah Data)
![Screenshot_20241125_080451_Chrome](https://github.com/user-attachments/assets/0cb4f09e-258d-4817-bb50-a14460a35563)
1. Definisi Fungsi:

     def tambah_data(mahasiswa): mendefinisikan sebuah fungsi bernama tambah_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2. Input NIM:

    nim = input("Masukkan NIM mahasiswa: ") meminta pengguna untuk memasukkan NIM (Nomor Induk Mahasiswa) dari mahasiswa yang akan ditambahkan. Nilai ini disimpan dalam variabel nim.
    
3. Input Nama:

   nama = input("Masukkan nama mahasiswa: ") meminta pengguna untuk memasukkan nama mahasiswa. Nilai ini disimpan dalam variabel nama.

4. Input Nilai Tugas, UTS, dan UAS:

   tugas = float(input("Masukkan nilai tugas: ")) meminta pengguna untuk memasukkan nilai tugas dan mengkonversinya menjadi tipe data float agar dapat melakukan perhitungan desimal. uts = float(input("Masukkan nilai UTS: ")) dan uas = float(input("Masukkan nilai UAS: ")) melakukan hal yang sama untuk nilai UTS dan UAS.

5. Menghitung Nilai Akhir:

  nilai_akhir = hitung_nilai_akhir(tugas, uts, uas) memanggil fungsi hitung_nilai_akhir yang telah didefinisikan sebelumnya, dengan parameter nilai tugas, UTS, dan UAS. Fungsi ini akan menghitung nilai akhir berdasarkan bobot yang telah ditentukan (tugas: 30%, UTS: 35%, UAS: 35%).

6. Menambahkan Data ke Dictionary:

  mahasiswa[nim] = {'nama': nama, 'tugas': tugas, 'uts': uts, 'uas': uas, 'nilai_akhir': nilai_akhir} menambahkan data mahasiswa ke dalam dictionary mahasiswa dengan menggunakan NIM sebagai kunci. Nilai dari kunci ini adalah sebuah dictionary yang berisi nama, nilai tugas, UTS, UAS, dan nilai akhir.

7. Pesan Konfirmasi:

 print("Data mahasiswa berhasil ditambahkan.") menampilkan pesan konfirmasi kepada pengguna bahwa data mahasiswa telah berhasil ditambahkan.

# 2. Menampilkan menu (Ubah Data)
![Screenshot_20241125_080512_Chrome](https://github.com/user-attachments/assets/62a94319-e94b-4272-8f99-c337b88fd1f4)
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
![Screenshot_20241125_080525_Chrome](https://github.com/user-attachments/assets/5d4fc372-4b39-403a-8d38-e35538ed21ae)
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
![Screenshot_20241125_080540_Chrome](https://github.com/user-attachments/assets/15e288d6-72b1-4754-838e-8d65f63d9894)
1. Definisi Fungsi:

def tampilkan_data(mahasiswa): mendefinisikan sebuah fungsi bernama tampilkan_data, yang menerima satu parameter yaitu mahasiswa. Parameter ini diharapkan berupa dictionary yang menyimpan data mahasiswa.

2. Pengecekan Data Kosong:

if not mahasiswa: memeriksa apakah dictionary mahasiswa kosong. Jika kosong, maka program akan menampilkan pesan bahwa tidak ada data mahasiswa yang tersedia.

3. Menampilkan Data:

Jika ada data mahasiswa, program akan menampilkan pesan "Data Mahasiswa:" sebagai header. for nim, data in mahasiswa.items(): melakukan iterasi melalui setiap item dalam dictionary mahasiswa. nim adalah kunci (NIM mahasiswa), dan data adalah nilai (dictionary yang berisi informasi mahasiswa).

4. Menampilkan Informasi Mahasiswa:

Di dalam loop, program akan mencetak informasi mahasiswa dengan format yang jelas: print(f"NIM: {nim}") menampilkan NIM mahasiswa. print(f"Nama: {data['nama']}") menampilkan nama mahasiswa. print(f"Nilai Tugas: {data['tugas']}") menampilkan nilai tugas. print(f"Nilai UTS: {data['uts']}") menampilkan nilai UTS. print(f"Nilai UAS: {data['uas']}") menampilkan nilai UAS. print(f"Nilai Akhir: {data['nilai_akhir']}") menampilkan nilai akhir yang telah dihitung.

# 5. Menampilkan menu (Cari Data)
![Screenshot_20241125_080553_Chrome](https://github.com/user-attachments/assets/4b1635e4-f426-4639-9754-4d219c139bd2)
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
![389179305-121ed05d-d51d-458d-b46d-dc19ac64384c](https://github.com/user-attachments/assets/e68a5497-de60-45d5-8394-ab69e55a58ee)
