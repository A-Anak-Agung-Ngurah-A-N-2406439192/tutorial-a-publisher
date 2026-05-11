# Tutorial A - Publisher

## Berapa banyak data yang dikirim publisher ke message broker dalam satu kali run?

Publisher mengirim 5 event/pesan ke message broker dalam satu kali run. Setiap event yang dikirim berupa `UserCreatedEventMessage`.

## Apa arti URL yang sama, yaitu `amqp://guest:guest@localhost:5672`?

URL tersebut berarti publisher dan subscriber terhubung ke message broker RabbitMQ yang sama, yaitu RabbitMQ yang berjalan di komputer lokal.

Pada URL `amqp://guest:guest@localhost:5672`:

- `guest` pertama adalah username.
- `guest` kedua adalah password.
- `localhost` berarti RabbitMQ berjalan di komputer lokal.
- `5672` adalah port default yang digunakan RabbitMQ untuk koneksi AMQP.

Karena publisher dan subscriber menggunakan URL broker yang sama serta nama event/queue yang sama, maka subscriber dapat menerima pesan yang dikirim oleh publisher.

![img1.png](img1.png)

![img.png](img2.png)

![img.png](img3.png)