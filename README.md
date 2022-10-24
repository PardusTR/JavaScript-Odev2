# JavaScript Odev - 02

Bu repo [Patika.Dev](www.patika.dev) JS Egitimindeki ikinci odevdir.

## HTML Ayrintisi

*Oncelikle HTML tarafini kontrol ediyoruz.*

```
<!DOCTYPE html>
<html lang="tr">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/css/style.css" />
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/css/bootstrap.min.css"
      integrity="sha384-B0vP5xmATw1+K9KRQjQERJvTumQW0nPEzvF6L/Z6nronJ3oUOFUFpCjEUQouq2+l"
      crossorigin="anonymous"
    />
    <title>Yapılacaklar Listesi</title>
  </head>
  <body>
    <div class="mr-1" style="position: relative">
      <div style="position: absolute; top: 0; right: 0">
        <div
          id="liveToast"
          class="toast success hide"
          role="alert"
          aria-live="assertive"
          aria-atomic="true"
          data-delay="4000"
        >
          <div>
            <button
              type="button"
              class="close"
              data-dismiss="toast"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="toast-body">Listeye eklendi.</div>
        </div>
      </div>
    </div>
    <div class="mr-1" style="position: relative">
      <div style="position: absolute; top: 0; right: 0">
        <div
          id="liveToast"
          class="toast error hide"
          role="alert"
          aria-live="assertive"
          aria-atomic="true"
          data-delay="4000"
        >
          <div>
            <button
              type="button"
              class="close"
              data-dismiss="toast"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="toast-body">Listeye boş ekleme yapamazsınız!</div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="header">
        <img
          src="https://cdn.sanity.io/images/9kdepi1d/production/65c832d202a503b15d99e628f4313782f3ef50db-300x62.png"
          class="mb-1"
          alt=""
        />
        <h2>Yapılacaklar Listesi</h2>
        <input type="text" id="task" placeholder="Bugün ne yapacaksın?" />
        <span onclick="newElement()" id="liveToastBtn" class="button"
          >Ekle</span
        >
      </div>

      <ul id="list">
        <li>3 Litre Su İç</li>
        <li>Ödevleri Yap</li>
        <li>En Az 3 Saat Kodlama Yap</li>
        <li>Yemek Yap</li>
        <li>50 Sayfa Kitap Oku</li>
      </ul>
      <script
        src="https://code.jquery.com/jquery-3.5.1.slim.min.js"
        integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj"
        crossorigin="anonymous"
      ></script>
      <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-Piv4xVNRyMGpqkS2by6br4gNJ7DXjqk09RmUpJ8jgGtD7zP9yug3goQfGII0yAns"
        crossorigin="anonymous"
      ></script>

      <script 
        src="/js/betik.js"
      ></script>

    </div>
  </body>
</html>
```

## CSS Ayrintisi

*Saat tarafinin calismasi icin de boyle bir yazim kullaniyoruz.*

```
* {
  box-sizing: border-box;
}

ul {
  margin: 0;
  padding: 0;
}

ul li {
  cursor: pointer;
  position: relative;
  padding: 12px 8px 12px 40px;
  background: #eee;
  font-size: 18px;
  transition: 0.2s;
  list-style-type: none;

  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

ul li:nth-child(odd) {
  background: #f9f9f9;
}

ul li:hover {
  background: #ddd;
}

ul li.checked {
  background: #276678;
  color: #fff;
  text-decoration: line-through;
}

ul li.checked::before {
  content: "";
  position: absolute;
  border-color: #fff;
  border-style: solid;
  border-width: 0 2px 2px 0;
  top: 10px;
  left: 16px;
  transform: rotate(45deg);
  height: 15px;
  width: 7px;
}

.close {
  position: absolute;
  right: 0;
  top: 0;
  padding: 12px 16px 12px 16px;
}

.close:hover {
  background-color: #f78501;
  color: white;

}

.header {
  background-color: #f78501;
  padding: 30px 40px;
  color: white;
  text-align: center;
}

img {
  background-color: white;
}

.header:after {
  content: "";
  display: table;
  clear: both;
}

input {
  margin: 0;
  border: none;
  border-radius: 0;
  width: 75%;
  padding: 10px;
  float: left;
  font-size: 16px;
}

.button {
  padding: 10px;
  width: 25%;
  background: #d9d9d9;
  color: #555;
  float: left;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
  border-radius: 0;
}

.button:hover {
  background-color: #bbb;
}
```

## Lisans

[Lisans Secimi](https://choosealicense.com/)
$~$