# WhoIS API - Discover your IP details
`by ARJOS`

Read below for information on how to use our free API. For more information, visit our official [website](https://whois.arjos.com.br/).

---


## ⬇️ Installation

It is not necessary to install any specific plug to use our API. You can make HTTP requests of the GET type with the programming language of your choice.


## 🚀 Usage

### See an example using native JavaScript:

```javascript
let info = []
function getInfos() {
    return new Promise((resolve, reject) => {
        fetch("https://whois.arjos.com.br/api/", {
            method: 'GET',
            mode: 'cors',
            headers: {
                'Content-Type': 'application/json',
                'Origin': '*',
                'Access-Control-Allow-Origin': '*',
                'Access-Control-Allow-Headers': '*',
                'Access-Control-Allow-Methods': 'GET,POST,PUT,PATCH,DELETE',
                'Access-Control-Max-Age': '86400'
            }
        }).then(response => {
            return response.json();
        }).then(res => {
            resolve(res);
            info = res
            console.log(info)
        }).catch(err => {
            reject(err);
        });
    });
}
getInfos();
```

### See an example of payload API request:

```json
{
    "ip": "206.43.69.40",
        "country": {
        "country_name": "Brasil",
        "country_code": "BR",
        "country_capital": "Brasília",
        "emoji_flag": "🇧🇷",
        "currency": "BRL",
        "currency_symbol": "R$",
        "call_code": "55"
    },
    "location": {
        "region": "Sao Paulo",
        "region_code": "SP",
        "region_capital": "São Paulo",
        "city": "São Paulo",
        "zipcode": "01000",
        "timezone": "America/Sao_Paulo",
        "latitude": -23.6283,
        "longitude": -46.6409
    },
    "provider": {
        "isp": "TELEFÔNICA BRASIL S.A",
        "company": "Vivo",
        "as": "AS27699 TELEFÔNICA BRASIL S.A"
    },
    "device": {
        "browser": "Chrome",
        "browser_language": "PT",
        "os": "Mac OS X",
        "type": "Desktop"
    }
}
```

## 🌎 Live

* __[Website WhoIS - IP](https://whois.arjos.com.br)__

## 🧑🏻‍💻 Authors

- [@arjosweb](https://www.github.com/arjosweb)


## ⚖️ License

MIT License

Copyright (c) 2021 @ARJOSWEB - ARJOS.COM.BR

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

  