# my bash

Adalah setingan bash yang aku pakai pada OS `Linux mint` atau `ubuntu 20.04`.

Themes dimodifikasi dan sudah sesuai dengan selera saya tentunya.

`my bash` itu sekadar untuk penyebutan proyek ini, karena harus dikasih nama.

## Tampilan

![preview](https://raw.githubusercontent.com/banghasan/my-bash/main/2021-07-28_14-39.jpg)

- ada info baterai laptop
- ada kolom waktu terminal
- ada kolom info repo git, branch, dan perubahannya
- ada info ERROR jika terdapat kesalahan
- ada info lama eksekusi aplikasi

## Sistem

`my bash` menggunakan [ohmypost](https://ohmyposh.dev) sebagai aplikasi pengantarnya.

Sehingga disarankan untuk melihat atau membaca dokumentasi sumbernya.


Mengapa menggunakan **ohmypost**, padahal sudah lama pakai [Powerline](https://github.com/b-ryan/powerline-shell) ?

Karena:

- dibangun menggunakan [golang](https://golang.org/), performa lebih menjajikan (speed dll)
- tanpa dependecy apapun
- lebih mudah customisasi.
- documentasi bagus.

> Apakah untuk Windows jalan? Nggak tau, saya dah lama gak pake windows :-)

## Cara Pakai

Lima langkah menuju my bash

### 1. Install

Install **ohmypost** terlebih dahulu ke sistem :

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```

### 2. Themes

Install themes ini

```bash
mkdir -p ~/.poshthemes
wget https://github.com/banghasan/my-bash/raw/main/banghasan.omp.json -O ~/.poshthemes
```

### 3. Bash

Edit file `.bashrc` :

```bash
xed ~/.bashrc
```

Boleh juga pakai `nano` / `pico`, `vim`, atau apapun editor favoritmu.

Kemudian tambahkan:

```bash
eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/banghasan.omp.json)"
```

### 4. Font

Boleh di pasang pada sistem global, atau pada user aktif saja. Karena di aku laptop dipakai sendirian, maka aku pasang di user aktif.

Buat pada user aktif jika folder belum ada, bikin dahulu folder `fonts`:

```bash
mkdir -p ~/.fonts
```

> Jika di sistem global `sudo mkdir -p /usr/local/share/fonts/`

Download font di [https://www.nerdfonts.com/font-downloads](https://www.nerdfonts.com/font-downloads).

Pilih sesuai selera. Kemudian ekstrak, letakkan file di folder tersebut.

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

Cek: 

- [referensi path](https://ohmyposh.dev/docs/path)

### Mirror

- [BangHasan](https://git.banghasan.com/banghasan/my-bash)
- [Github](https://github.com/banghasan/my-bash)