# my bash

Adalah setingan bash yang aku pakai pada OS `Linux mint` atau `ubuntu 20.04`.

Themes dimodifikasi dan sudah sesuai dengan selera saya tentunya.

`my bash` itu sekadar untuk penyebutan proyek ini, karena harus dikasih nama.

## Tampilan


## Sistem

`my bash` menggunakan [ohmypost](https://ohmyposh.dev) sebagai aplikasi pengantarnya.

Sehingga disarankan untuk melihat atau membaca dokumentasi sumbernya.


### 1. Install

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```

### 2. Themes

Install themes `my bash` yang aku pakai:

```bash
mkdir ~/.poshthemes
wget URL -O ~/.poshthemes
```

### 3. Bash

Edit file `.bashrc` pakai editor favoritmu. Misalnya:

```bash
xed ~/.bashrc
```

Kemudian tambahkan:

```bash
eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/banghasan.omp.json)"
```

### 4. Font

Jika folder belum ada, bikin dahulu folder `~/.fonts`:

```bash
mkdir -p ~/.fonts
```

Download font di [https://www.nerdfonts.com/font-downloads](https://www.nerdfonts.com/font-downloads).

Pilih yang sesuai selera. Kemudian ekstrak, letakkan file di folder `~/.fonts` tersebut.

### 5. Sesuaikan

Edit preferences terminalnya, pilih font yang sesuai.

Selesai!

> Jika tidak ada perubahan, jangan lupa buka terminal baru untuk melihat hasilnya.

## Lain-lain

Jika pada tampilan **path** tidak ingin terlihat panjang (full), bisa di edit file json nya.

```json
{
    "type": "path",
    "style": "powerline",
    "powerline_symbol": "",
    "foreground": "#e4e4e4",
    "background": "#3465a4",
    "properties": {
        "prefix": " \uF07C ",
        "home_icon": "~",
        "style": "full"
    }
},
```        

pada bagian style bisa diganti menjadi: 

- agnoster
- agnoster_full
- agnoster_short
- full
- folder
- mixed
- letter

Dicoba-coba saja biar tahu efek nya :-)

Cek: [referensi](https://ohmyposh.dev/docs/path)