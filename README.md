# WhoIS API `by ARJOS`

Read below for information on how to use our free API. For more information, visit our official [website](https://whois.arjos.com.br/).

## Installation

It is not necessary to install any specific plug to use our API. You can make HTTP requests of the GET type with the programming language of your choice.

## Usage

See an example using native JavaScript:

```javascript
let info = []
function getInfos() {
    return new Promise((resolve, reject) => {
        fetch("https://whois.arjos.com.br/api/info", {
            method: 'GET',
            mode: 'cors',
            headers: {
                'Content-Type': 'application/json',
                'Origin': '*',
                'Access-Control-Allow-Origin': '*',
                'Access-Control-Allow-Headers': '*',
                'Access-Control-Allow-Methods': 'POST,PUT,PATCH,DELETE',
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

See an example using jQuery:

```javascript
$.ajax({
  type: "GET", 
  headers: {
    'Content-Type': 'application/json',
    'Origin': '*',
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Headers': '*',
    'Access-Control-Allow-Methods': 'POST,PUT,PATCH,DELETE',
    'Access-Control-Max-Age': '86400'
  },
  dataType: "json",
  url: 'https://whois.arjos.com.br/info/',
  success: function(data) {
    console.log(
      'Your ip address is ' + data.ip
        + ' city: ' + data.city
        + ' region: ' + data.region_name
        + ' country: ' + data.country_name
    );
    
  }
});
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

## Copyright

All right reserved for [**ARJOS Devepment**](https://github.com/arjosweb) (Artur Medeiros).