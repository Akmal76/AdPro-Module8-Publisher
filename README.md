# Tutorial 8 - Advanced Programming - Publisher
**Akmal Ramadhan - 2206081534 - Kelas A**

## Berapa banyak data yang terkirim?
Program _publisher_ akan mengirim sebanyak lima data ke _message broker_ untuk tiap sekali _run_. Hal ini karena pada `main` terdapat lima `publish_event` dan setiap `publish_event` mengirim satu `UserCreatedEventMessage` ke _message broker_.

## _Publisher_ dan _Subscriber_ mengakses URL yang sama. Apa artinya?
_Publisher_ dan _subscriber_ mengakses yang sama yaitu `amqp://guest:guest@localhost:5672` maka keduanya mengakses _server_ AMQP yang sama. Dengan kata lain, keduanya saling berkomunikasi dengan _message broker_ yang sama. Pesan yang dikirim oleh _publisher_ akan diterima oleh _subscriber_ yang terhubung ke _server_.

## Message Broker dengan RabbitMQ
### Running RabbitMQ as message broker
<img src="image/img_0.png">

### Sending and Processing Event
<img src="image/img_1.png">

Pada saat _message broker_ atau RabbitMQ berjalan, ketika program Subscriber dan Publisher kita jalankan (`cargo run`), maka Publisher akan mengirimkan data ke _message broker_ dan Subscriber akan menerima data tersebut. Pada gambar di atas, kita dapat melihat bahwa Publisher mengirimkan data sekali ke _message broker_ dan Subscriber menerimanya.

### Monitoring chart based on publisher."
<img src="image/img_2.png">

Pada gambar di atas, saya mencoba untuk _run_ Publisher berkali-kali sehingga _message rates_-nya meningkat lalu untuk beberapa detik kemudian saya mencoba melakukan _run_ dua kali dengan waktu jeda yang agak lama. Dari apa yang saya lakukan, saya pahami bahwa **_message rates_ akan meningkat ketika Publisher mengirimkan data ke _message broker_**. Jika _message rates_ tinggi, maka _message broker_ akan menerima banyak data dari Publisher.

## Referensi
- Module 8 - Software Architecture oleh Ade Azurat dan Tim Pengajar.