Flowchartnya


![tugas 5](https://user-images.githubusercontent.com/56390857/72361221-b0558880-3723-11ea-8d95-f6139ab62e0c.JPG)


Untuk kodingnya =

data = {}
print("Program Input Nilai")
print("===================")
while True:
    d = input("(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : ")
    if d.lower() == 't':
        print("Tambah Data")
        nama = input("Nama : ")
        NIM = input("NIM : ")
        tugas = int(input("Nilai Tugas : "))
        uts = int(input("Nilai UTS : "))
        uas = int(input("Nilai UAS : "))
        a = int(tugas * 30 / 100)
        b = int(uts * 35 / 100)
        c = int(uas * 35 / 100)
        akhir = a + b + c
        data[nama] = [nama, NIM, tugas, uts, uas, akhir]
        print(data)
    elif d.lower() == 'l':
        print("Lihat nilai")
        print("===================================================================================")
        print("| No. |     Nama     |      NIM     |   Tugas   |   UTS   |   UAS   |    Akhir    |")
        print("===================================================================================")
        no = 1
        if data.keys():
            for x in data.values():
                print("|  {:2} |  {nama:10}  |  {NIM:10}  |   {tugas:5}   |   {uts:3}   |   {uas:3}   |    {akhir:3.2f}    |".format(no, nama=x[0], NIM=x[1], tugas=x[2], uts=x[3], uas=x[4], akhir=x[5]))
                no += 1
        else:
            print("|                                  TIDAK ADA DATA                                 |")
        print("===================================================================================")
    elif d.lower() == 'k':
        break
    elif d.lower() == 'h':
        print("Hapus data")
        nama = input("Nama : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data nilai untuk anak yang bernama {0} tidak ada".format(nama))
    elif d.lower() == 'u':
        print("Ubah data")
        nama = input("Nama : ")
        if nama in data.keys():
            NIM = input("NIM : ")
            tugas = int(input("Nilai Tugas : "))
            uts = int(input("Nilai UTS : "))
            uas = int(input("Nilai UAS : "))
            data[nama][1] = NIM
            data[nama][2] = tugas
            data[nama][3] = uts
            data[nama][4] = uas
        else:
            print("Data nilai untuk anak yang bernama {0} tidak ada". format(nama))
    elif d.lower() == 'c':
        print("Cari data")
        nama = input("Nama : ")
        if nama in data.keys():
           print("=============================================================================")
           print("|     Nama     |      NIM     |   Tugas   |   UTS   |   UAS   |    Akhir    |")
           print("=============================================================================")
           print("|  {nama:10}  |  {NIM:10}  |   {tugas:5}   |   {uts:3}   |   {uas:3}   |    {akhir:3.2f}    |".format(nama=data[nama][0],
NIM=data[nama][1],tugas=data[nama][2], uts=data[nama][3], uas=data[nama][4], akhir=data[nama][5]))
           print("=============================================================================")
        else:
            print("Data nilai untuk anak yang bernama {0} tidak ada".format(nama))
    else:
        print("Pilih menu yang tersedia")
        
        
  Hasilnya seperti dibawah ini
  
  ![5-hasil](https://user-images.githubusercontent.com/56390857/72361114-84d29e00-3723-11ea-850f-3befdf31c75c.JPG)
