# praktikum8

![Screenshot (188)](https://user-images.githubusercontent.com/116137169/207383488-e406787e-c68d-488b-8e7d-fe3ed0c021c6.png)

# rumus :
       class mahasiswa:
    def __init__(self, nim, nama, tugas, uts, uas):
        self.nim = nim
        self.nama = nama
        self.tugas = tugas
        self.uts = uts
        self.uas = uas

    def tambah(self,nim,nama,tugas,uts,uas):
        data.nim.append(nim)
        data.nama.append(nama)
        data.tugas.append(tugas)
        data.uts.append(uts)
        data.uas.append(uas)

    def lihat(self):
        for i in range(len(data.nama)):
            print("|", i+1, "  |", end="")
            print('{0:<25}'.format(self.nama[i]), end="")
            print("|", self.nim[i], end="")
            print(" |", self.tugas[i], end="")
            print("    |", self.uts[i], end="")
            print("  |", self.uas[i], " | ", end="")
            print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")

    def ubah(self,nim,nama,tugas,uts,uas):
        self.nim[no] = nim
        self.nama[no] = nama
        self.tugas[no] = tugas
        self.uts[no] = uts
        self.uas[no] = uas

    def hapus(self):
        del self.nim[no]
        del self.nama[no]
        del self.tugas[no]
        del self.uts[no]
        del self.uas[no]

    data = mahasiswa([],[],[],[],[])

    while True:
    menu = input("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar]:")
    if menu == "t" or menu == "T":
       print("\nTambah Data")
       data.tambah(
           input("Masukkan NIM : "),
           input("Masukkan Nama : "),
           int(input("Nilai Tugas : ")),
           int(input("Nilai UTS : ")),
           int(input("Nilai UAS : "))
           )
       print("\nData berhasil ditambahkan")

    elif menu == "l" or menu == "L":
        print("\nDaftar Nilai")
        print("==========================================================================")
        print("| No  |          Nama           |    NIM    | TUGAS | UTS | UAS |  AKHIR |")
        print("==========================================================================")
        if len(data.nama) != 0:
            data.lihat()
        else:
            print("                         TIDAK ADA DATA                               ")
        print("==========================================================================")

    elif menu == "u" or menu == "U":
        print("\nUbah Data")
        ubah = input("Masukkan Nama : ")
        if ubah in data.nama:
           no = data.nama.index(ubah)
           print("Masukkan Data Yang Baru : ")
           data.ubah(
               input("NIM : "),
               input("Nama : "),
               int(input("Nilai Tugas : ")),
               int(input("Nilai UTS : ")),
               int(input("Nilai UAS : "))
               )
        else:
            print(ubah, "tidak ada di dalam data")

    elif menu == "h" or menu == "H":
        print("\nHapus Data")
        hapus = input("Masukkan Nama : ")
        if hapus in data.nama:
            no = data.nama.index(hapus)
            data.hapus()
            print("Data", hapus, "Berhasil dihapus")
        else:
            print(hapus, "tidak ada di dalam data")

    elif menu == "k" or menu == "K":
        print("\nTerimakasih\n")
        break

    else:
        print("\nPerintah yang dimasukkan salah!\n")
    
# screanshoot program
![Screenshot (189)](https://user-images.githubusercontent.com/116137169/207385045-8ffe6818-7297-49fd-91be-eaf8631c2c4f.png)
![Screenshot (190)](https://user-images.githubusercontent.com/116137169/207385511-ab411ace-005f-4eec-9417-cb0aceb300a8.png)
![Screenshot (191)](https://user-images.githubusercontent.com/116137169/207385558-b9593f5a-dcc4-4ed3-9025-c5e4a107475b.png)
![Screenshot (192)](https://user-images.githubusercontent.com/116137169/207385600-5294d25f-1cb6-4b43-aeeb-dd694ea7fa02.png)
 # HASIL RUN/PENJELUASAN
METHODE TAMBAH DATA(t)
 ![Screenshot (196)](https://user-images.githubusercontent.com/116137169/207386916-b248296b-49fa-482e-87d6-b3266c050bcd.png)
 deklarasikanlah Class  mahasiswa yang mempunyai objek NIM, Nama, nilai tugas, nilai UTS dan nilai UAS masukanlah fungsi def __init dan self
 deklarasikanlah kotak kolom untuk pilihan yang akan di input
 disini saya memasukan 5 kotak pilihan
 
        data = mahasiswa([],[],[],[],[])
        
Kita akan membuat beberapa method untuk menambahkan, menampilkan, menghapus, mengubah data mahasiswa. Pertama membuat method tambah(), method ini berfungsi untuk menambahkan data. Dalam cara ini kita menggunakan append() supaya data yang terakhir ditambahkan ada di urutan list paling akhir.

      def tambah(self,nim,nama,tugas,uts,uas):
              data.nim.append(nim)
              data.nama.append(nama)
              data.tugas.append(tugas)
              data.uts.append(uts)
              data.uas.append(uas)

# METHODE LIHAT DATA(l)
 ![Screenshot (197)](https://user-images.githubusercontent.com/116137169/207392385-fc785ae3-f7d2-4cfc-b476-22a1fda79b72.png)
fungsi Lihat untuk menampilkan seluruh data yang sudah di input
dengan logika jika data tidak ditemukan maka akan muncul tulisan "TIDAK ADA DATA"

               def lihat(self):
        for i in range(len(data.nama)):
            print("|", i+1, "  |", end="")
            print('{0:<25}'.format(self.nama[i]), end="")
            print("|", self.nim[i], end="")
            print(" |", self.tugas[i], end="")
            print("    |", self.uts[i], end="")
            print("  |", self.uas[i], " | ", end="")
            print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")
            
# METHODE UBAH DATA(u)
![Screenshot (198)](https://user-images.githubusercontent.com/116137169/207394304-cb0b40a9-5fc8-443a-b942-26e097b1abef.png)
fungsi ubah untuk merubah data yang sudah di input dengan rumus


           print("\nUbah Data")
        ubah = input("Masukkan Nama : ")
        if ubah in data.nama:
           no = data.nama.index(ubah)
           print("Masukkan Data Yang Baru : ")
           data.ubah(
               input("NIM : "),
               input("Nama : "),
               int(input("Nilai Tugas : ")),
               int(input("Nilai UTS : ")),
               int(input("Nilai UAS : "))
               )
        else:
            print(uba![Screenshot (199)](https://user-images.githubusercontent.com/116137169/207396015-2ad26f4f-897b-4d26-8c5b-dcf43a0ad953.png)
            h, "tidak ada di dalam data")

# METHODE HAPUS DATA(h)
 ![Screenshot (199)](https://user-images.githubusercontent.com/116137169/207398138-12ee388c-8b89-405e-b2de-57b7dcafd010.png)


terakhir kita membuat method hapus(), yang berfungsi untuk menghapus data berdasarkan nama. Kita bisa menggunakan del untuk menghapus datanya. Seperti sebelumnya, daftar indeks nomor yang akan dihapus disesuaikan dengan inputan dari user. Yaitu indeks nomor ke - (no).
               def hapus(self):
        del self.nim[no]
        del self.nama[no]
        del self.tugas[no]
        del self.uts[no]
        del self.uas[no]

# diagram
![image](https://user-images.githubusercontent.com/116137169/207396627-85adf1e7-e0f0-44f3-a5f0-d86a70f0a5f0.png)

# flowchart
![image](https://user-images.githubusercontent.com/116137169/207396808-cdb7eee9-cd5a-439f-a212-f45552b29bb8.png)
