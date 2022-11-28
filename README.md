Nama : Wisnu Ikhwansyah Saputra

Nim : 312210305

Kelas : TI 22.A3

---

# Praktikum 6

Masukan Input : 

    mahasiswa = {}
    
    
    def show():
        if mahasiswa.items():
            print("Daftar Nilai")
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            i = 0
            for a in mahasiswa.items():
                i += 1
                print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
                      .format(a[0][: 14], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no=i))
            print("=================================================================================")
    
        else:
            print("Daftar Nilai")
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            print("|                                TIDAK ADA DATA                                 |")
            print("=================================================================================")
    
    
    def add():
        print("Tambah Data")
        nama = input("Nama\t : ")
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir
    
    
    def delete():
        print("Hapus Data")
        nama = input("Masukkan Nama : ")
    
        if nama in mahasiswa.keys():
            del mahasiswa[nama]
    
        else:
            print("Nama tidak ditemukan")
    
    
    def update():
        print("Ubah Data")
        nama  = input("Masukkan Nama : ")
        if nama in mahasiswa.keys():
            nim = input("NIM\t : ")
            uts = int(input("Nilai UTS\t : "))
            uas = int(input("Nilai UAS\t : "))
            tugas = int(input("Nilai Tugas\t : "))
            akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
            mahasiswa[nama] = nim, tugas, uts, uas, akhir
    
        else:
            print("Nama tidak ditemukan ")
    
    
    def search():
        print("Cari Data")
        a = input("Masukkan Nama : ")
        if a in mahasiswa.keys():
            print("===========================================================================")
            print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
            print("===========================================================================")
            print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
                  .format(a, mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4]))
            print("===========================================================================")
    
        else:
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            print("|                          DATA TIDAK DITEMUKAN                                 |")
            print("=================================================================================")
    
    
    def menu():
        print("\n")
        print("================================")
        print("      Program input nilai       ")
        print("================================\n")
    
        x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
        print("\n")
    
        if x == 'L':
            show()
        elif x == 'T':
            add()
        elif x == 'U':
            update()
        elif x == 'H':
            delete()
        elif x == 'C':
            search()
        elif x == 'K':
            print("==========================================================================")
            print('\n')
            print("> You exit the code                        ")
            print("\n")
            print("==========================================================================")
    
            exit()
    
        else:
            print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")
    
    
        while True:
        menu()
        
Maka outputnya akan menjadi seperti berikut 

Input Nilai : 

<img width="376" alt="input nilai" src="https://user-images.githubusercontent.com/110619093/204196012-1a109348-be0f-405e-8254-702ee645f0fe.png">

Lihat Nilai : 

<img width="507" alt="lihat nilai" src="https://user-images.githubusercontent.com/110619093/204196053-4c7e1bcd-6dc1-48e4-8db9-41df8102c5be.png">

---

## Latihan

Masukan input sebagai berikut : 

    telepon = {
        'Thor' : '086969969',
        'Loki' : '08234562'
    }
    
    print(telepon['Thor'])
    
    print("\n")
    
    telepon['Heimdal'] = '0813345643'
    telepon['Surtr'] = '0824574123'
    
    print(telepon.keys())
    print(telepon.values())
    
    print("\n")
    
    print("Nama\t| Nomor Telepon ")
    print("======================")
    
    for nama,nomor in telepon.items():
        print("%s \t| %s " % (nama,nomor))
    
    print("\n")
    
    del telepon['Heimdal']
    
    print("Nama\t| Nomor Telepon")
    print("======================")
    for key,val in telepon.items():
        print("%s \t| %s " % (key,val))
        
Maka outputnya akan jadi seperti ini :

<img width="402" alt="latihan" src="https://user-images.githubusercontent.com/110619093/204196319-23ce9fa0-dc37-4904-bceb-56b131185dc7.png">
