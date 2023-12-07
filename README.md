# pert-12
<p>Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah
class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:</p>
<p>- Method tambah() untuk menambah data</p>
<p>- Method tampilkan() untuk menampilkan data</p>
<p>- Method hapus(nama) untuk menghapus data berdasarkan nama</p>
<p>- Method ubah(nama) untuk mengubah data berdasarkan nama</p>
<p>Buat diagram class, flowchart dan penjelasan programnya pada
README.md.</p>
<p>Commit dan push repository ke github.</p>
<p>masukkan kode program </p>

data={} 
import os
class data_mahasiswa():
    def tambah():
        print(f"{'Tambah Data':^17}")
        print('='*17)
        nim = str(input('NIM\t\t: '))
        nama = str(input('Nama\t\t: '))
        uts = int(input('Nilai UTS\t: '))
        uas = int(input('Nilai UAS\t: '))
        tugas = int(input('Nilai Tugas\t: '))
        akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)
        data[nama]=nim, uts, uas, tugas, akhir
    def tampilkan():
        print(f"{'Daftar Data Mahasiswa':^82}")
        print('='*84)
        print(f"|{'NO':^4}|{'NIM':^20}|{'NAMA':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")
        print('='*84)
        n = 0
        for a in data.items():
            n += 1
            print("|{no:^4}|{0:^20}|{1:^20}|{2:^10}|{3:^6}|{4:^6}|{5:^10}|"
            .format(a[1][0], a[0][:13], a[1][1], a[1][2], a[1][3], a[1][4], no = n))
        print('='*84)

    def hapus(nama):
        print(f"{'Data Berhasil di Hapus':^17}")
        print('='*17)
        del data[nama]

    def ubah(nama):
        print(f"{'Ubah Data':^17}")
        print('='*17)
        nim = str(input('NIM\t\t: ')) 
        uts = int(input('Nilai UTS\t: '))
        uas = int(input('Nilai UAS\t: '))
        tugas = int(input('Nilai Tugas\t: '))
        akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)
        data[nama] = nim, uts, uas, tugas, akhir

    def salah():
        print(f"{'Daftar Data Mahasiswa':^82}")
        print('='*84)
        print(f"|{'NO':^4}|{'NIM':^20}|{'NAMA':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")
        print('='*84)
        print(F"|{'Tidak ada data':^82}|")
        print('='*84)
while True:
    print()
    lanjut = str(input('MENU\n=======\n(L)ihat\n(T)ambah\n(U)bah\n(H)apus\n(K)eluar\n=======\nPilihan : '))
    os.system("cls")
    if lanjut.lower() == 'l':
        if data.items():
            data_mahasiswa.tampilkan()
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 't':
            data_mahasiswa.tambah()
    elif lanjut.lower() == 'h':
        print('Data yang ingin di hapus')
        nama = str(input('Nama\t\t: '))
        if nama in data.keys():
            data_mahasiswa.hapus(nama)
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 'u':
        print('Data yang ingin di ubah')
        nama = str(input('Nama\t\t: '))
        if nama in data.keys():
            data_mahasiswa.ubah(nama)
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 'k':
        break
    else :
        print('Pilih menu yang tersedia')
print('Program Selesai')
    

# <p>program tambah data </p>
![image](https://github.com/ekarahayu24/pert-12/assets/147680283/322e2465-0310-4d1f-bcab-b5f7eca1fa35)

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/d5bcf4f6-34b3-4a2d-966a-b0de93d8ad0b)

# <p>program tampilkan data</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/3b349f77-9d78-4544-9620-b4c82b067717)

# <p>program hapus data</p>
<p>masukkan data yang ingin dihapus </p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/edc28684-e8fa-4d02-b85e-97df9c29b116)

# <p>program ubah data</p>
<p>masukkan data yang ingin diubah</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/3f25505d-e272-4f7a-9c31-614a452ae406)

# <p>tampilan data yang sudah diubah</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/0189b39f-59a8-46a8-b15e-088eb3e137b5)

# <p>keluar program</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/5ed67b54-fa1f-46b2-ab72-04a2267e13e5)


<p>tampilan diagram kelas</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/d5e70249-0e2e-49d6-a928-afe1a3c4e559)

<p>tampilan flowchart</p>

![image](https://github.com/ekarahayu24/pert-12/assets/147680283/530378ee-8200-4e2e-9a84-29f6ed94f952)











