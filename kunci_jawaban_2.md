# Kunci jawaban tugas 2 pasep
 1. smbpasswd -a namauser
 2. hanya nama pengguna yang terdaftar
 3. /etc/apt/sources.list.d/
 4. Opsi pilihan
   a. Layanan dnsmasq sedang berjalan, tetapi direktif interface=ens34 hilang atau salah ketik (misal: ens33) di file konfigurasi.
   c. Konfigurasi dhcp-range di dnsmasq.conf salah ketik, tidak valid, atau tidak mencakup subnet 192.168.11.0/24.
   e. Layanan dnsmasq tidak berjalan (statusnya dead atau failed) setelah server di-reboot.
 5. Opsi pilihan 
  b. File smb.conf di bagian [shared] tidak memiliki baris writable = yes (atau diatur ke no).
  c. User 'joni' ada di Linux, tetapi belum ditambahkan ke database Samba menggunakan smbpasswd -a joni.
  e. File smb.conf di bagian [shared] memiliki baris valid users = @staff, dan 'joni' bukan anggota grup staff.
 6. Opsi pilihan
  a. Solusinya adalah menonaktifkan systemd-resolved (systemctl disable --now systemd-resolved) agar port 53 bebas sepenuhnya untuk dnsmasq.
  b. dnsmasq gagal karena mencoba binding ke port 53 (misal: 0.0.0.0:53 atau 192.168.11.1:53) yang sudah terisi sebagian oleh systemd-resolved.
  d. dnsmasq gagal karena systemd-resolved adalah layanan yang lebih modern dan memiliki prioritas lebih tinggi. 
7. Opsi pilihan
 b. dhcp-option=3,192.168.11.1
 c. dhcp-range=192.168.11.100,192.168.11.200,12h
 d. interface=ens34
8. anonymous_enable=NO
9. apt install samba
10. write_enable=YES
11. SFTP (SSH File Transfer Protocol)
12. Menetapkan 'root' sebagai pemilik folder, tetapi memberikan hak akses grup kepada 'sambashare'. Siapa pun anggota grup 'sambashare' dapat mengakses sesuai izin grup.
13. Untuk memiliki cadangan file konfigurasi asli (default) jika terjadi kesalahan konfigurasi, sehingga mudah untuk dikembalikan seperti semula.
14. Di dalam file /var/lib/misc/dnsmasq.leases.
15. Menambahkan protokol lama seperti server min protocol = NT1 dan ntlm auth = yes.
16. systemctl restart sshd (atau ssh)
17. Opsi pilihan
 a. userlist_enable=YES DAN userlist_deny=NO, dengan file vsftpd.userlist berisi "joni" dan "susi".
 b. write_enable=YES
 c. chroot_local_user=YES
18. Memastikan bahwa file/folder baru yang dibuat di dalam direktori tersebut akan secara otomatis mewarisi kepemilikan grup dari direktori induk (bukan grup primer pembuat file).
19. Sebuah server online yang menyimpan kumpulan paket perangkat lunak (aplikasi dan library) yang siap diinstal.
20. Subnet Mask (misal: 255.255.255.0).
21. Karena dnsmasq lebih ringan, konfigurasinya lebih sederhana, dan sudah mengintegrasikan fungsi DHCP dan DNS dalam satu layanan.
22. cname=www.toko.lokal,toko.lokal
23. Sebagai 'pintu keluar' atau router yang harus dituju klien jika ingin terhubung ke internet.
24. apt update
25. mkdir /srv/data




