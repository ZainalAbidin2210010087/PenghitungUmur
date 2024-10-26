
Nama		: Zainal Abidin


NPM		: 2210010087


Kelas		: 5B Nonreg Banjarmasin


Mata Kuliah	: Pemrograman Berbasis Objek 2


# latihan 2 (Membuat Aplikasi Penghitung Umur)

1. di sini saya menggunakan "JFrameForm" untuk tampilan utama aplikasi


2. Komponen yang saya gunakan antara lain adalah :
- JLabel untuk Memberi nama pada Label "Tanggal Lahir","Umur",Dan "Hasil"
- JDateChooser untuk memilih "Tanggal Lahir"
- JButton Dengan teks "Hitung" agar dapat memproses Umur Berdasarkan Tanggal    Lahir Yang dipilih
- JTextField Untuk Menampilkan Hasil Umur Dalam Format Tahun,Bulan,dan Hari


 
3.Atur Layout:
 Atur layout komponen pada "JFrame" sesuai kebutuhan.
 Disini saya mengatur komponen, dengan "JDateChooser" di sebelah "JLabel" "Tanggal Lahir", "JButton" "Hitung", dan "JTextField" untuk hasil "umur".



4.Pada tahap awal saya memasukan fungsi impor yaitu:
"import java.time.LocalDate;
import java.time.Period;
import java.util.Date;
import com.toedter.calendar.JDateChooser;"



5.Untuk koding tombol hitung :
"private void hitungUmurActionPerformed(java.awt.event.ActionEvent evt) {
    Date tanggalLahir = jDateChooser.getDate();
    LocalDate lahir = tanggalLahir.toInstant().atZone(ZoneId.systemDefault()).toLocalDate();
    LocalDate sekarang = LocalDate.now();

    Period selisih = Period.between(lahir, sekarang);
    umurField.setText(selisih.getYears() + " Tahun " + selisih.getMonths() + " Bulan " + selisih.getDays() + " Hari");
}"
