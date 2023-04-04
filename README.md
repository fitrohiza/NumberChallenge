# Challenge Function Number Javascript

## Table of Contents

- [Random Number](#random)
- [Rounding Number](#round)
- [Numeric Test](#numeric)
- [Round Up 5](#roundUp)

## Random Number <a name = "random"></a>

Pada file randomNumber.js terdapat sebuah function bernama rand yang memiliki 2 buah parameter berupa min dan max. didalam function rand terdapat sebuah fungsi pengecekan menggunakan if.

```javascript
if (min == null && max == null) {
  return 0;
}
```

jika argumen min dan max bernilai null atau kosong maka akan mengembalikan nilai 0. kemudian terdapat satu pengecekan kondisi lagi.

```javascript
if (max == null) {
  max = min;
  min = 0;
}
```

dimana apabila nilai max null atau kosong dan nilai min memiliki nilai maka nilai max akan mengambil nilai min dan nilai min akan di set menjadi 0.
setelah pengecekan kondisi, function rand akan mengembalikan sebuah nilai random menggunakan salah satu fungsi math di javascript :

```javascript
return Math.floor(Math.random() * (max - min + 1)) + min;
```

Pada kode diatas digunakan Math.floor() yang digunakan untuk membulatkan bilangan desimal menjadi bilangan bulat ke bawah. Dengan fungsi ini, bilangan acak yang dihasilkan akan dibulatkan menjadi bilangan bulat. Sedangkan Math.random() menghasilkan sebuah bilangan acak antara 0 dan 1. max - min + 1 digunakan untuk menghitung rentang bilangan acak yang ingin dihasilkan, yaitu rentang antara nilai maksimum (max) dan nilai minimum (min) yang diinginkan. sedangkan + min digunakan untuk menambahkan nilai min untuk memastikan bahwa rentan yang dimaksud masih sesuai.

## Rounding Number <a name = "round"></a>

```javascript
const rounding = function (n, b) {
  let result = n.toFixed(b);
  return result;
};
```

pada file rounding.js terdapat sebuah anonymouse function yang memiliki 2 parameter berupa n dan b. didalam function tersebut terdapat sebuah variabel result yang nilainya akan memotong nilai dibelakang koma pada argument n mengikuti nilai pada argument b. Jika argument b bernilai 2 maka jumlah angka dibelakang koma pada argument b akan berjumlah 2 digit.

## Numeric Test <a name = "numeric"></a>

```javascript
function isItNumeric(input) {
  return !isNaN(parseFloat(input)) && isFinite(input);
}
```

pada file numerikTest.js terdapat sebuah function isItNumeric yang memiliki 1 parameter berupa input. Didalam function tersebut akan mengembalikan nilai dengan salah satu fungsi javascript yaitu isNaN yang digunakan untuk mengecek apakah sebuah nilai bernilai NaN. Jika iya maka nilai tersebut bukanlah numerik.

## Round Up 5 <a name = "roundup"></a>

```javascript
function roundUpToFive(input) {
  return Math.ceil(input / 5) * 5;
}
```

pada file roundUp.js terdapat sebuah function roundUpToFive yang memiliki 1 parameter berupa input. Didalam function tersebut akan mengembalikan nilai input dengan salah satu fungsi Math.ceil yang digunakan untuk untuk membulatkan nilai input ke atas dengan nilai integer terdekat yang lebih besar dari nilai input. Karena yang diminta adalah pembulatan dalam kelipatan 5 maka nilai input akan dibagi 5 dan dikali 5.
