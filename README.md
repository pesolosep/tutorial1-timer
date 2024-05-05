# tutorial1-timer


![alt text](<img/hey hey.png>)

Output dihasilkan seperti di atas karena program melakukan `println` terlebih dahulu pada `"hey hey"` lalu melakukan `drop spawner` dan menjalankan executor untuk mengerjakan tasknya, sehingga async task selalu berjalan setelah println "hey hey".

![alt text](<img/multiple with drop(spawner).png>)

Menambahkan multiple spawner akan membuat executor menjalankan 3 asynchronous tasks secara bersamaan, menghasilkan sebuah output yang tidak dapat diprediksi karena sifatnya yang concurrent. Dikarenakan adanya `drop(spawner)` maka executor akan terus berjalan sampai queue kosong.

![alt text](<img/multiple with drop(spawner).png>)

Mirip seperti diatas, akan tetapi program akan terus berjalan karena walaupun queue kosong executor akan terus menunggu task berikutnya dari spawner dan tidak menutup spawn.