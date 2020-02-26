# fdhlmhd.github.io

# Markdown Bootcamp DampCorp

## Cara Instalasi Git di Linux
Disini saya menggunakan Ubuntu versi 18.04 LTS , bisa di download di https://ubuntu.com/download

### Langkah instalisasi 
 
   Sebelum meng-install Git, update dulu Linux Ubuntu untuk upgrade package :
```sh
$ sudo apt-get update
```
Setelah itu kita bisa instal Git :
```sh
$ sudo apt-get install git
```
Tunggu tuh sampe selesai , jika sudah cek apakah git sudah terinstal :
```sh
$ git --version
```
### Konfigurasi Git
Untuk Konfigurasi Git , bisa di atur dengan menyiapkan username dan email :
```sh
$ git config --global user.name "Usernamebebasweh"
$ git config --global user.email bebaswe@example.com
```
gampang ih.. lanjut.

### Perintah dasar Git

##### git init
Perintah ini wajib ya jangan sampe lupa , untuk membuat repo baru . skuy :
```sh
$ git init
```
##### git add 
Perintah git add digunakan untuk menambahkan file ke index , skuy :

nah ini untuk menambahkan file tertentu :
```sh
$ git add bebasweh.js
```

kalau ini untuk menambahkan semua yang ada pada folder target :

```sh
$ git add .
```
atau
```
$ git add -A
```
sama aja sih , cuman ada cara untuk mengecualikan file yang kita tidak inginkan untuk di tambahkan 
```sh
$ touch.gitignore
```
maka akan terbuat file .gitignore , nanti tambahkan didalam file tersebut dengan cara copy syntax di sumber ini , sesuaikan dengan apa yang di butuhkan . https://github.com/github/gitignore/tree/master/Global 

#### git commit 
Perintah ini pasti tidak asing lagi , perubahan apapun yang di -commit tidak akan langsung ke remote repository. skuy :

```sh
$ git commit -m "bebas we nyak"
$ git commit --amend -m "bebas weh"
```
#### git remote 
Perintah git remote ini untung menghubungkan ke repository user yang ingin kita remote, bingung ? coba dulu skuy :

```sh
$ git remote add origin https/:isi lnk repo target
```

cek dulu supaya menampilkan repo yang sedang di konfigurasi :

```sh
$ git remote -v
```

#### git branch
Perintah ini bisa di gunakan untuk membuat branch baru atau menghapus branch.
untuk melihat branch yang ada , ketik ini :
```sh
$ git branch
```
untuk menghapus branch :
```sh
$ git branch -d <nama-branch>
```
untuk menambah branch :
```sh
$ git checkout -b "nama"
```

#### git clone
perintah ini untuk clone repository , kek download gitu skuy :

```sh
$ git clone <repo> 
```
jika ingin di masukan ke folder tertentu tinggal tambahkan nama folder setelah repo.

#### git push
Perintah git Push akan mengirimkan perubahan ke master branch dari remote repository yang berhubungan dengan direktori. skuy:
```sh
$ git push origin master
```
#### git pull
Perintah ini untuk menggabungkan semua perubahan yang ada di remote repo , ke direktori lokal
```sh
$ git pull origin master
```
##### Untuk colaborasi dengan team jangan lupa invite anggota team di setting > manage access > masukan email

### untuk mengatasi pull request yang konflik
ikuti langkah berikut :
```sh
> git fetch origin namabranch:namabranch
> checkout ke branch
> git rebase origin/master
> git add .
> git rebase --continue
> git push -f origin <nama-branch>
```
