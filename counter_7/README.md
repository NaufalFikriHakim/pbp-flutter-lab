# counter_7
## Tugas 7
### Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.
- Stateless widget adlaah widget yang dimuat secara statis. Seluruh konfigurasi yang dimuat didalamnya telah diinisiasikan sejak awal widget tersebut dibuat. Stateless widget adalah sebuah widget yang tidak dapat diubah dan tidak akan pernah berubah.
- Stateful widget merupakan suatu widget yang sifatnya dinamis atau dapat berubah-ubah, kebalikan dari stateless widget. Stateful widget dapat mengubah tampilan, menambah widget, mengubah nilai variabel, icon, warna, dan lain-lain.

### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
1. Text: Menampilkan Teks
2. Column: Menampung widget dan disusun secara vertikal
3. Row: Menampung widget dan disusun secara horizontal
4. FloatingActionButton: Widget button yang berada di depan widget lainnya
5. Icon: Menampilkan suatu ikon
6. Center: Layout widget yang berfungsi untuk menengahkan childnya

### Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
setState() berfungsi untuk mengubah suatu state yang ada di stateful widget. Variabel yang terdampak di fungsi tersebut adalah _counter.

### Jelaskan perbedaan antara const dengan final.
Final harus diinisiasikan terlebih dahulu, tidak bisa diubah valuenya, dan harus sudah diketahui valuenya pada saat run time. Sedangkan, const bisa diubah valuenya dan valuenya diketahui pada saat compile time.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
1. Membuat projek dengan `flutter create counter_7`
2. Membuat fungsi untuk mendecrement counter
3. Menambahkan widget FloatingActionButton kedua untuk mendecrement dan akan hilang apabila counternya = 0
4. Membuat Text berwarna merah ketika counter % 2 = 0, dan biru ketika tidak terpenuhi. 

## Tugas 8

### Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement.
`Navigator.push` akan menambahkan (push) sebuah rute ke tumpukan (_stack_) Navigator. Sedangkan `Navigator.pushReplacement` akan mengganti rute yang sedang ditampilkan dengan *push* route atau halaman baru ke stack Navigator.
### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
`TextFormField` field untuk menerima input dari user. <br>
`Drawer` sebagai hamburger menu untuk navigasi ke page berbeda. <br>
`DropdownButtonFormField` sebagai dropdown untuk menentukan input yang diberikan merupakan pemasukan atau pengeluaran. <br>
`FloatingActionButton` sebagai button yang di-bind untuk menambah data ke dalam list <br>
`Card` untuk menampilkan data input yang ada pada list.
### Sebutkan jenis-jenis event yang ada pada Flutter (contoh: onPressed).
1. `onPressed()`
2. `onTap()`
3. `onChanged()`
4. `onSaved()`
### Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter.
Navigator bekerja seperti struktur data stack, yaitu konsep _Last In First Out_. Setiap tampilan akan di-_push_ ke stack Navigator untuk ditampilkan. Jadi, tampilan yang ditampilkan merupakan halaman yang terakhir di-_push_ atau berada pada posisi paling atas pada stack.
### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
1. Membuat widget drawer untuk navigasi ke halaman lain.
2. Membuat file form.dart untuk menerima input dari user. Judul dan Nominal menerima input menggunakan TextFormField sementara untuk tipe pemasukan dan pengeluaran menggunakan DropdownButtonFormField.
3. Membuat FloatingActionButton yang di-bind untuk menyimpan input. Selain itu, mem-validasi apakah input sudah terisi benar atau belum.
4. Menambahkan input yang sudah tervalidasi ke dalam list data.
5. Membuat data.dart untuk menampilkan data input yang sudah disimpan.
5. Mengimport file .dart agar list input data dapat diakses pada data.dart.
6. Menampilkan data pada list dengan menggunakan builder ListView.builder().
7. Membuat Card untuk menampilkan judul, nominal, jenis budget.

## Pertanyaan Tugas 9

### Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?

Bisa, tetapi kita tidak bisa memastikan apakah data JSON yang diambil sudah memiliki bentuk seperti yang kita inginkan. Sehingga akan lebih baik apabila kita membuat model terlebih dahulu.

### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.

1. Checkbox membuat checkbox yang memiliki suatu event onChange
2. Expanded membuat text tidak overflow
3. FutureBuilder membuat widget berdasarkan snapshot yang diambil dari Future

### Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter.

Menambahkan depedensi http, kemudian melakukan GET pada data json yang selanjutnya dikonversikan ke dalam suatu model yang dibuat. Data json kemudian ditampilkan dengan menggunakan FutureBuilder.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

1. Menambahkan navigasi ke mywatchlist pada drawer
2. Menambahkan depedency http
3. Membuat model untuk data json
4. Membuat function untuk mengambil data json
5. Menampilkan data dalam bentuk inkwell
6. Membuat halaman detail untuk watchlist

