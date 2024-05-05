# tutorial1-timer

![alt text](<img/Screenshot 2024-05-05 215419.png>)

Output dihasilkan seperti di atas karena program melakukan `println` terlebih dahulu pada `"hey hey"` lalu melakukan `drop spawner` dan menjalankan executor untuk mengerjakan tasknya, sehingga async task selalu berjalan setelah println "hey hey".

