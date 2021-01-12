# UAS1

NAMA : HENDRI FAZRi

KELAS : TI. 20. B2

NIM : 312010291

Soal UAS diantaranya ;

![screen 1](/gambar/screen1.png)

Dan ini adalah hasil pacekage yang saya buat

![screen 2](/gambar/screen2.png)

SOAL 1 (Daftar_Nilai)

Pada soal pertama, dibawah ini saya telah menyantumkan beberapa syntax yang nantinya akan menghasilkan semua
modul dari package Daftar_Nilai yang diantaranya adalah (Tambah Data, Ubah Data, Hapus Data, Dan Cari Data)

print("========Program Input Nilai =========")
data={}
while True:
    print("")
    c =input("(L)lihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : ")
    if c.lower() == 'k':
        print("Keluar Program")
        break

    elif c.lower() == 'l':
        if data.items():
            print("Daftar Nilai Mahasiswa")
            print("================================================================================================")
            print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
            print("================================================================================================")
            i=0
            for x in data.items():
                i+=1
                print(" | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |"
                      .format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
                print("================================================================================================")
        else:
            print("Daftar Nilai Mahasiswa")
            print("================================================================================================")
            print("| NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
            print("================================================================================================")
            print("|                                      TIDAK ADA DATA                                         |")
            print("================================================================================================")

    elif c.lower() == 't':
        print("=======Tambah Data=======")
        nama    =input("Nama                :  ")
        nim     =input("Nim                 :  ")
        tugas   =int(input("masukan nilai tugas :  "))
        uts     =int(input("masukan nilai uts   :  "))
        uas     =int(input("masukan nilai uas   :  "))
        akhir   = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
        data[nama] = nim ,tugas, uts, uas, akhir
        print("=========================")

    elif c.lower() == 'u':
        print('=======Ubah Data Mahasiswa=======')
        nama = input('Nama                :  ')
        if nama in data.keys():
            nim     =input('Nim                 :  ')
            tugas   =int(input("masukan nilai tugas :  "))
            uts     =int(input("masukan nilai uts   :  "))
            uas     =int(input("masukan nilai uas   :  "))
            akhir   =(0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
            data[nama] = nim, tugas, uts, uas, akhir
        else:
            print("Data Nilai Tidak Ada".format(nama))
        print("=================================")

    elif c.lower() == 'h':
        print("====hapus data mahasiswa====")
        nama=input("nama :  ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data Nilai Tidak Ada".format(nama))
        print("============================")

    elif c.lower() == 'c':
        print("===cari data mahasiswa===")
        nama=input("Masukan Nama :  ")
        if nama in data.keys():
            print("Daftar Nilai Mahasiswa")
            print("======================================================================================")
            print(" |     NAMA      |    NIM     |    TUGAS    |     UTS     |     UAS     |  AKHIR   | ")
            print("======================================================================================")
            print(" | {0:12s}  | {1:10} | {2:11d} | {3:11d} | {4:11d} | {5:8.2f} |"\
                   .format(nama, nim, tugas, uts, uas, akhir))
            print("======================================================================================")
        else:
            print("Data {0} Tidak tersedia ".format(nama))

    else:
        print(" === Pilih Sesuai Menu Yang Tersedia === ")
		
		Disini saya akan mencoba untuk menguraikannya. Pertama untuk menghasilkan modul Tambah Data kamu perlu
		memasukan syntax dibawah ini.
		
		 elif c.lower() == 't':
        i = open('database.txt','a')
        P(" Tambah Kontak")
        while (True):
            nama = input(" Nama : ")
            if nama == '':
                P(' Masukan dengan Nama Dengan Benar')
            else:
                break
        while (True):
            try:
                nim  = int(input(" NIM  : "))
                if nim == '':
                    P(' Masukan Nim dengan Angka')
            except ValueError:
                P(' Masukan Nim dengan Angka')
            else:
                break
        while (True):
            try:
                tugas  = int(input(" TUGAS  : "))
                if tugas == '':
                    P(' Masukan TUGAS dengan Angka')
            except ValueError:
                P(' Masukan TUGAS dengan Angka')
            else:
                break
        while (True):
            try:
                uts  = int(input(" UTS  : "))
                if uts == '':
                    P(' Masukan UTS dengan Angka')
            except ValueError:
                P(' Masukan UTS dengan Angka')
            else:
                break
        while (True):
            try:
                uas  = int(input(" UAS  : "))
                if uas == '':
                    P(' Masukan UAS dengan Angka')
            except ValueError:
                P(' Masukan UAS dengan Angka')
            else:
                break
        akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
        i.write('\nNama : '+nama+'|Nim : '+str(nim)+'|Tugas : '+str(tugas)+'|UTS : '+str(uts)+'|UAS : '+str(uas)+"|Akhir : "+str(akhir)+'\n')
        i.close()
		
		
Disini saya akan mencoba untuk menguraikannya. Pertama untuk menghasilkan modul Tambah Data kamu perlu
memasukan syntax dibawah ini.
		
		    elif c.lower() == 't':
        i = open('database.txt','a')
        P(" Tambah Kontak")
        while (True):
            nama = input(" Nama : ")
            if nama == '':
                P(' Masukan dengan Nama Dengan Benar')
            else:
                break
        while (True):
            try:
                nim  = int(input(" NIM  : "))
                if nim == '':
                    P(' Masukan Nim dengan Angka')
            except ValueError:
                P(' Masukan Nim dengan Angka')
            else:
                break
        while (True):
            try:
                tugas  = int(input(" TUGAS  : "))
                if tugas == '':
                    P(' Masukan TUGAS dengan Angka')
            except ValueError:
                P(' Masukan TUGAS dengan Angka')
            else:
                break
        while (True):
            try:
                uts  = int(input(" UTS  : "))
                if uts == '':
                    P(' Masukan UTS dengan Angka')
            except ValueError:
                P(' Masukan UTS dengan Angka')
            else:
                break
        while (True):
            try:
                uas  = int(input(" UAS  : "))
                if uas == '':
                    P(' Masukan UAS dengan Angka')
            except ValueError:
                P(' Masukan UAS dengan Angka')
            else:
                break
        akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
        i.write('\nNama : '+nama+'|Nim : '+str(nim)+'|Tugas : '+str(tugas)+'|UTS : '+str(uts)+'|UAS : '+str(uas)+"|Akhir : "+str(akhir)+'\n')
        i.close()
Jadi kesimpulannya jika kalian menggunakan semua syntax yang saya tunjukan diawal dan memasukan 'T' pada
kolom yang tersedia dan kalian run, maka akan mendapat output seperti dibawah ini, yang dimana itu adalah hasil
untuk menambahkan data.


![screen 3](/gambar/screen3.jpg)

Kedua untuk menghasilkan modul Ubah Data kamu perlu memasukan syntax dibawah ini.

 elif c.lower() == 'u':
        u = open('database.txt','r').read().splitlines()
        target = input(' Masukan Nama : ')
        nm = []
        for l in u:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                if na == target:
                    P(' Mengedit Data %s'%(target))
                    while (True):
                        nama = input(" Nama : ")
                        if nama == '':
                            P(' Masukan dengan Nama Dengan Benar')
                        else:
                            break
                    while (True):
                        try:
                            nim  = int(input(" NIM  : "))
                            if nim == '':
                                P(' Masukan Nim dengan Angka')
                        except ValueError:
                            P(' Masukan Nim dengan Angka')
                        else:
                            break
                    while (True):
                        try:
                            tugas  = int(input(" TUGAS  : "))
                            if tugas == '':
                                P(' Masukan TUGAS dengan Angka')
                        except ValueError:
                            P(' Masukan TUGAS dengan Angka')
                        else:
                            break
                    while (True):
                        try:
                            uts  = int(input(" UTS  : "))
                            if uts == '':
                                P(' Masukan UTS dengan Angka')
                        except ValueError:
                            P(' Masukan UTS dengan Angka')
                        else:
                            break
                    while (True):
                        try:
                            uas  = int(input(" UAS  : "))
                            if uas == '':
                                P(' Masukan UAS dengan Angka')
                        except ValueError:
                            P(' Masukan UAS dengan Angka')
                        else:
                            break
                    akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
                    edit  =('Nama : '+nama+'|Nim : '+str(nim)+'|Tugas : '+str(tugas)+'|UTS : '+str(uts)+'|UAS : '+str(uas)+"|Akhir : "+str(akhir)+'\n')
                    nm.append(edit+'\n')
                else:
                    nm.append(str(l)+'\n')
        new = open('database.txt','w')
        new.write(str(nm))
        new.close()
        new = open('database.txt','r').read().splitlines()
        new1 = open('database.txt','w')
        new1.close()
        new2 = open('database.txt','a')
        for i in new:
            i2 = i.replace("['","").replace("\\n', '", "\n").replace("']","").replace("\\n","\n")
            new2.write(i2+'\n')
        new2.close()
	
Jadi kesimpulannya jika kalian menggunakan semua syntax yang saya tunjukan diawal dan memasukan 'U' pada
kolom yang tersedia dan kalian run, maka akan mendapat output seperti dibawah ini, yang dimana itu adalah hasil
untuk mengubah data.

![screen 4](/gambar/screen4.jpg)

Ketiga untuk menghasilkan modul Hapus Data kamu perlu memasukan syntax dibawah ini.

 elif c.lower() == 'h':
        u = open('database.txt','r').read().splitlines()
        target = input(' Masukan Nama : ')
        nm = []
        for l in u:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                if str(na) == str(target):
                    P('BERHASIL MENGHAPUS Data %s'%(target))
                    pass
                else:
                    nm.append(str(l)+'\n')
        new = open('database.txt','w')
        new.write(str(nm))
        new.close()
        new = open('database.txt','r').read().splitlines()
        new1 = open('database.txt','w')
        new1.close()
        new2 = open('database.txt','a')
        for i in new:
            i2 = i.replace("['","").replace("\\n', '", "\n").replace("']","").replace("\\n",'')
            new2.write(i2)
        new2.close()
	
Jadi kesimpulannya jika kalian menggunakan semua syntax yang saya tunjukan diawal dan memasukan 'H' pada
kolom yang tersedia dan kalian run, maka akan mendapat output seperti dibawah ini, yang dimana itu adalah hasil
untuk menghapus data.

![screen 5](/gambar/screen5.jpg)

Untuk mencari data itu sendiri kalian hanya perlu memasukan inisial dari modul tersebut. Misalkan kalian ingin
mencari moodul untuk Menghapus Data, maka kamu hanya perlu memasukan huruf 'H' pada kolom yang tersedia.

SOAL 2 (View_Nilai)

Untuk menjawab soal nomer 2, kalian hanya perlu mengetikan huruf "L" pada kolom yang di sediakan untuk melihat
hasil pencarian ataupun daftar nilai. Maka nanti akan mendapatkan hasil output seperti gambar dibawah ini.

![screen 6](/gambar/screen6.jpg)

SOAL 3 (Input_Nilai)

Pada soal ke-3 ini, jika kalian ingin menginput suatu data yaitu sama halnya seperti kalian memasukan huruf "T"
untuk menambahkan suatu data. Dan hasil output yang dihasilkan pun sama yaitu sebagai berikut.

![screen 7](/gambar/screen7.jpg)
