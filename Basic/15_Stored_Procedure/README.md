# SQL Stored Procedure

Stored Procedure adalah sebuah sekumpulan syntax SQL yang dimana kita bisa memanggilkan kapanpun. Stored Procedure (selebihnya kita singkat dengan SP) memiliki kelebihan yaitu keamanan dan juga kecepatan. Aman karena tidak semua orang bisa mengakses langsung SP ini. Kecepatan karena SP adalah sebuah syntax SQL yang dicompile.

## Sample Pembuatan dan Pemanggilan SP

**_disini saya menggunakan Microsoft SQL Server_**

```sql
CREATE PROCEDURE NAMA_PROCEDURE
AS
BEGIN
  SELECT DATA FROM TABLE_X1
END
```

Sangat simple bukan? Selanjutnya bagaimana untuk memanggil syntax tersebut?

```sql
EXEC NAMA_PROCEDURE
```

## Mengapa harus SP?

Jika kita lihat syntax diatas, maka terlihat sangat simple sekali, teman teman disini akan berfikir kenapa tidak langsung menggunakan native SQL di coding ataupun ORM, begini saya jelaskan

### Complicated Data

Terkadang kita memiliki raw data yang terlalu complicated dan tambah harus melakukan join ke beberapa table, maka dari itu SP adalah sebuah solusi yang mumpuni dan juga cepat, dengan begitu backend hanya akan memanggil SP dan frontend akan langsung mendapatkan return datanya.

### Cepat

Seperti yang dijelaskan sebelumnya, SP adalah sebuah kumpulan syntax SQL yang di-compile, maka dari itu bisa dibilang, dari sisi DB, ini sangat cepat.