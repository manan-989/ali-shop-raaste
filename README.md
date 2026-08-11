[README.md](https://github.com/user-attachments/files/30934012/README.md)
# ali-shop-raaste

**Ali Mobile Shop Toolkit** ke bahar wale pate (raaste) — sirf aik file: `raaste.json`

---

## Ye repo kis liye hai

Toolkit ki exe **98 MB** ki hai. Pehle MovieBox ka pata (`moviebox.ph`,
`h5-api.aoneroom.com`) code ke andar likha hua tha. Jis din site apna naam
badalti, har customer ki app chup ho jati aur sab ko nayi 98 MB ki exe
bhejni parti.

Ab pata is repo ki file mein hai. App ise **din mein aik dafa** khud parhti
hai. Yani:

> Site ka naam badle → yahan aik line badlein → har customer ki app agle din
> khud theek ho jayegi. **Nayi exe bhejne ki zarurat NAHI.**

---

## Zaroori: file ka pata na badlein

App bilkul is pate par file dhoondti hai:

```
https://raw.githubusercontent.com/manan-989/ali-shop-raaste/main/raaste.json
```

Yani teen cheezein waisi hi rehni chahiyen:

| Cheez | Kya honi chahiye |
|---|---|
| Repo ka naam | `ali-shop-raaste` |
| Branch | `main` |
| File | `raaste.json` — repo ki **jarh** mein (kisi folder ke andar nahi) |
| Repo | **Public** (private ho to app parh nahi sakegi) |

Inme se koi bhi badla to app ko file milna band ho jayegi (aur wo khamoshi se
apne andar wale purane pate par chalti rahegi).

---

## Pata kaise badlein

Maan lein MovieBox `moviebox.ph` se `moviebox.pk` par chala gaya. Sirf itna:

```json
"siteHosts": [
  "moviebox.pk"
]
```

Bas. Commit karein. Ho gaya.

- `https://` likhne ki zarurat nahi — app khud laga leti hai.
- Poori file likhna zaroori nahi. Jo khana file mein na ho, app uske liye
  apni purani qeemat istemal kar leti hai. Yani sirf **jo badla hai** wohi
  likhna kaafi hai.
- `version` ka number aik barha dein (`2` → `3`) — is se app ke "Raaste"
  safhe par nazar aa jata hai ke nayi file lag chuki hai.

---

## App ye khane parhti hai

Baqi sab (jinke naam `_` se shuru hote hain) sirf samajhne ke liye likhai
hai — app unhein chhorh deti hai.

```
version
updated
moviebox.apiHosts          <- dhoondne wali API ka pata
moviebox.siteHosts         <- site ka apna pata (page + link dono)
moviebox.bffPath
moviebox.pagePath          <- ismein {detailPath} hona LAZMI hai
moviebox.endpoints.search
moviebox.endpoints.download
moviebox.headers.x-request-lang
quality.poochhne_ki_hadd_mb
```

### `pagePath` ka khayal rakhein

Is mein `{detailPath}` zaroor hona chahiye. Wo na ho to har movie/drama ka
pata aik hi ban jayega aur download bilkul band ho jayegi. App is ki jaanch
karti hai — agar `{detailPath}` gayab ho to wo poori line chhorh kar apni
purani qeemat par wapas chali jati hai.

---

## Galti ho jaye to kya hoga

**Kuch nahi tootega.** App teen jagah dekhti hai, isi tarteeb mein:

1. **Ye file** (sab se nayi)
2. **Pichhli dafa utri hui copy** — internet band ho to yehi chalti hai
3. **Exe ke andar likhe purane pate** — ye kabhi khali nahi hote

Comma ghalat lag jaye, file adhoori ho, repo delete ho jaye, internet band
ho — har surat mein app neeche wale darje par chali jati hai aur chalti
rehti hai. Kabhi bilkul nahi rukti.

---

## Foran chahiye to

App khud roz dekhti hai. Agar intezar nahi karna:

App kholein → **Raaste** safha → **Abhi dekho** ka button.

Wahin ye bhi nazar aata hai ke abhi kaunsa pata chal raha hai aur wo kahan
se aaya — GitHub se, utri hui copy se, ya exe ke andar se.
