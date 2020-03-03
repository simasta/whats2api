# W2API - WhatsApp REST API 

Welcome to best REST API for WhatsApp. 
This library provide you an complete solution for WhatsApp REST API without any necessities of code or change anything, obviously, if you want, you can contribute but give this information for us over PR. - Important to know, it's not an official solution - if you need something professional please don't use this package.

Special thanks to developers of amazing packages used here, Mohammed Shah [(smashah)](https://github.com/smashah) and Total.js [(totaljs)](https://github.com/totaljs)

## SETUP

This package was thought to be used as service for each connection, so you need to understand the structure of files and folders before start - please read with attention.

Each connection with WhatsApp will need an dedicated running of this, you can run a lot of connections on the same server using PM2 or forever. For better approach too we will provide you an Docker solution.

Each client is undertood as INSTANCE, we gonna set an instance NUMBER for him, to identify after if necessary. If you are running this probably you need to receive messages, the struture of receive will be over WEBHOOK post events, so you need to configure your preffered address too. (TIP: use some service as https://requestcatcher.com/ to test ). Another important thing to set is some TOKEN, this is used for protect your inbound endpoint. For a high level of changes you will need to set an MASTERKEY too, that can be used to do profound changes on server like restarts and force stops.

### Configuring the enviroment
To start - download the package, open /config file and set variables below - please respect type of variables or your code will not run properly

```javascript
//WhatsApp Configurations		
instance            : 83430
webhook             : http://localhost:3000
token               : j19ksi1mim1lksm12213
masterKey           : w2apiisthebestlibrary
```

### Start te project

```bash
> npm install && node debug.js
```
### Documentation
Full documentation library can be found here and over postaman 

[Documentation](https://choosealicense.com/licenses/mit/)

[Postman Collection](https://choosealicense.com/licenses/mit/)

## Using Library
All the examples below are provided in CURL to allow as many users as possible to enjoy the solutions created, however if you use any specific language feel free to download the Postman collection here and get the code in its best language for you.


### Sending messages
```javascript
curl --location --request POST 'localhost:8000/83430/sendMessage?token=j19ksi1mim1lksm12213' \
--header 'Content-Type: application/json' \
--data-raw '{
	"chatId":"PHONE_NUMBER@c.us",
	"body": "W2API - Best REST API for WhatsApp"
}'
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)


## Legal

This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by WhatsApp or any of its affiliates or subsidiaries. This is an independent and unofficial software. Use at your own risk.

## Cryptography Notice

This distribution includes cryptographic software. The country in which you currently reside may have restrictions on the import, possession, use, and/or re-export to another country, of encryption software. BEFORE using any encryption software, please check your country's laws, regulations and policies concerning the import, possession, or use, and re-export of encryption software, to see if this is permitted. See [http://www.wassenaar.org/](http://www.wassenaar.org/) for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has classified this software as Export Commodity Control Number (ECCN) 5D002.C.1, which includes information security software using or performing cryptographic functions with asymmetric algorithms. The form and manner of this distribution makes it eligible for export under the License Exception ENC Technology Software Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section 740.13) for both object code and source code.

