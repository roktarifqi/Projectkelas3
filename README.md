**MEMBUAT WEB HOTEL DENGAN PHP**

1. users → reservasi.pengguna_id
Seorang user (tamu hotel) melakukan reservasi.
Data pemesanan tersebut dicatat di tabel reservasi.
Kolom pengguna_id di tabel reservasi menunjuk ke id dari user tersebut di tabel users.
Artinya:
"User memesan kamar → datanya dicatat di tabel reservasi, dengan referensi siapa yang memesan."

2. reservasi → kamar
Setiap reservasi menyertakan kamar_id yang mengarah ke kamar yang dipesan.
Ini menjelaskan bahwa reservasi tersebut terkait langsung dengan kamar tertentu.
Artinya:
"Reservasi berkaitan dengan kamar mana yang dipesan."

4. users → transaksi.kasir_id
Seorang kasir memproses pembayaran dari reservasi.
Identitas kasir dicatat di kolom kasir_id pada tabel transaksi.
Kolom tersebut juga merujuk ke id pada tabel users.
Artinya:
"Transaksi pembayaran dilakukan oleh user yang berperan sebagai kasir."

4. transaksi → reservasi
Setiap transaksi mengacu pada satu reservasi.
Hubungan ini dicatat melalui kolom reservasi_id di tabel transaksi.
Artinya:
"Transaksi adalah pembayaran atas reservasi tertentu."

6. log_admin → users
Tabel log_admin bersifat opsional, digunakan untuk mencatat aktivitas yang dilakukan oleh admin.
Kolom admin_id merujuk ke users.id, tapi hanya digunakan jika role = 'admin'.
Artinya:
"Aktivitas penting yang dilakukan admin dicatat dalam log."
