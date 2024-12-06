# **Streams Builder**

## Nama : Sukma Bagus Wahasdwika

## NIM  : 2241720223

## **Praktikum - Dart StreamsBuilder**

### **Soal 12:**
* Jelaskan maksud kode pada langkah 3 dan 7 ! 
    **Jawab:**

    *Langkah 3 :*
    - NumberStream adalah sebuah kelas yang menyediakan stream angka secara periodik.
    - getNumber() adalah metode yang menghasilkan (yield) stream angka dengan tipe int.
    - Stream.periodic digunakan untuk menghasilkan event secara periodik, yaitu setiap 1 detik (Duration(seconds: 1)).
    Di setiap event, Stream.periodic memanggil fungsi callback (int t), di mana:
    - Random random = Random(); membuat sebuah objek untuk menghasilkan angka acak.
    - random.nextInt(10) menghasilkan angka acak antara 0 sampai 9.
    - yield* digunakan untuk meneruskan semua nilai dari stream yang dihasilkan oleh Stream.periodic.
    Intinya: Metode ini akan mengirimkan angka acak setiap 1 detik melalui stream.

    *Langkah 7:*
    - stream: numberStream: StreamBuilder menerima numberStream (stream angka dari langkah 3).
    - initialData: 0: Data awal yang ditampilkan di layar sebelum stream mulai menghasilkan angka.
    - builder: (context, snapshot): Fungsi builder yang digunakan untuk membangun widget berdasarkan data terbaru (snapshot) dari stream.
    - if (snapshot.hasData) pertama: Kondisi ini menampilkan pesan Error! di konsol setiap kali ada data pada snapshot, tetapi tidak memiliki efek lain pada UI.
    if (snapshot.hasData) kedua:
    - Jika data tersedia, widget akan menampilkan teks angka terbaru dari stream.
    - snapshot.data berisi angka terbaru dari stream.
    - Text(snapshot.data.toString(), style: TextStyle(fontSize: 96)) menampilkan angka dalam ukuran font besar di tengah layar.
    - else:
    Jika tidak ada data, maka widget akan menampilkan SizedBox.shrink(), yaitu widget kosong.


* Capture hasil praktikum Anda berupa GIF dan lampirkan di README.

    ![alt text](gif/streambuilderhasil.gif)
