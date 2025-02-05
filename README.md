### Sort, Dir, Limit, Page => `Digunakan Untuk Get Api List`
1. Sort => `sort=user_id` 
2. Dir => `dir=ASC` => `Sort user_id ASC`
3. Dir => `dir=DESC` => `Sort user_id DESC`
4. Limit => default 10 => `limit=10`
5. Page => default 1 => `page=1`
6. search => `search=bakwan`



## Respon API

#### HTTP CODE
- 200 ( Untuk respon berhasil )
- 400 ( Untuk respon gagal )
- 412 ( Untuk respon gagal validasi form input)
- 401 ( Untuk token tidak valid / expired )
- 403 ( Untuk refresh token tidak valid / expired)

#### GET List Respon Sukses
- Note : next_page = 0, Jika sudah di halaman akhir.
```
{
    "status": 200,
    "message": "Data Ditemukan.",
    "validation": {},
    "result": {
        "data": [],
        "pagination":{
            "total_data": 9,
            "total_page": 1,
            "next_page": 0,
        }
    }
}
```

#### GET Detail Respon Sukses
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 200,
    "message": "Detail Data Ditemukan.",
    "validation": {},
    "result": {}
}
```

#### GET Detail Respon Data Tidak Ditemukan
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 400,
    "message": "Detail Data Tidak Ditemukan.",
    "validation": {},
    "result": {}
}
```

#### POST/PATCH/PUT/DELETE Add Update Delete Respon Berhasil
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 200,
    "message": "Berhasil Add Update Delete Data",
    "validation": {},
    "result": {}
}
```

#### POST/PUT/PATCH/DELETE Add Update Delete Respon Gagal
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 400,
    "message": "Gagal Add Update Delete Data.",
    "validation": {},
    "result": {}
}
```

#### POST/PUT/PATCH/DELETE Add Update Delete Respon Eror Validasi
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 412,
    "message": "error_validation",
    "validation": {
       "username" : [
           "tidak boleh kosong",
           "hanya boleh alphabet"
       ]
    },
    "result": {}
}
```

#### POST/PUT/PATCH/DELETE/GET Respon Eror Auth
- Note : data dan message bisa di isi sesuai kebutuhan

```
{
    "status": 401,
    "message": "Anda tidak memiliki akses",
    "validation": {},
    "result": {}
}
```