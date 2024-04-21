# Tutorial 8 - Advanced Programming - Publisher
**Akmal Ramadhan - 2206081534 - Kelas A**

## Berapa banyak data yang terkirim?
Program _publisher_ akan mengirim sebanyak lima data ke _message broker_ untuk tiap sekali _run_. Hal ini karena pada `main` terdapat lima `publish_event` dan setiap `publish_event` mengirim satu `UserCreatedEventMessage` ke _message broker_.

## _Publisher_ dan _Subscriber_ mengakses URL yang sama. Apa artinya?
_Publisher_ dan _subscriber_ mengakses yang sama yaitu `amqp://guest:guest@localhost:5672` maka keduanya mengakses _server_ AMQP yang sama. Dengan kata lain, keduanya saling berkomunikasi dengan _message broker_ yang sama. Pesan yang dikirim oleh _publisher_ akan diterima oleh _subscriber_ yang terhubung ke _server_.

## Message Broker dengan RabbitMQ
### Running RabbitMQ as message broker
<img src="https://media.discordapp.net/attachments/1231573845731708940/1231573865189085204/image.png?ex=6626500a&is=6624fe8a&hm=6be41f7646f6e7d3f2877cc4b427c71fa095ef2737816a5cfe5cfd51ef0c7dfd&=&format=webp&quality=lossless&width=1100&height=662">

## Referensi
- Module 8 - Software Architecture oleh Ade Azurat dan Tim Pengajar.