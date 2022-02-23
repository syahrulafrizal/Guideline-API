### Sort, Dir, Limit, Page => `Digunakan Untuk Get Api List`
1. Sort => `sort=user_id` 
2. Dir => `dir=ASC` => `Sort user_id ASC`
3. Dir => `dir=DESC` => `Sort user_id DESC`
4. Limit => default 10 
5. Page => default 1



## Respon API
#### Data
- Pastikan tidak ada value yg null (didefault string kosong jika null)

#### HTTP CODE
- 200 ( Untuk semua respon )
- 401 ( Untuk token tidak valid / expired )

#### GET List Respon Sukses
```
{
    "status": 200,
    "message": "Data Ditemukan.",
    "results": {
        "data": [],
        "pagination":{
            "total_data": 9,
            "total_page": 1,
            "next_page": 0, // 0, Jika sudah di halaman akhir.
        }
    }
}
```

#### GET Detail Respon Sukses

```
{
    "status": 200,
    "message": "Detail Data Ditemukan.",
    "results": {
        "data": {}
    }
}
```

#### GET Detail Respon Data Tidak Ditemukan

```
{
    "status": 400,
    "message": "Detail Data Tidak Ditemukan.",
    "results": {
        "data": {}
    }
}
```

#### GET Add Update Delete Respon Berhasil

```
{
    "status": 200,
    "message": "Berhasil Add Update Delete Data",
    "results": {
        "data": {}
    }
}
```

#### GET Add Update Delete Respon Gagal

```
{
    "status": 400,
    "message": "Gagal Add Update Delete Data.",
    "results": {
        "data": {}
    }
}
```

#### GET Add Update Delete Respon Eror Validasi

```
{
    "status": 412,
    "message": "Nama tidak boleh kosong",
    "results": {
        "data": {}
    }
}
```
