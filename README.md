
https://ngrok.com/docs/getting-started/

for macos : 

1- intall ngrok : 
brew install ngrok

2- register for an acount on https://ngrok.com/docs/getting-started/

h*****i@hotmail.com    pass: ******



3- Run the following command to add your authtoken to the default ngrok.yml configuration file : 
ngrok config add-authtoken 2hdud76d5dh8lA9hgdujg0iOt3Xj_7KdUfNEbxd76sgdjkid

Authtoken will be saved to configuration file: /Users/macintosh/Library/Application Support/ngrok/ngrok.yml

4- now u can start deploying your app online : 
type in the terminal : 

ngrok http 8000

ngrok will start the tunnel and display the informations
and will display the local address  : Web interface 
and also the global address : forwarding
The public URL (https://7b51-94-187-0-7.ngrok-free.app)

now to test open a new terminal window (Cmd+N) keeping the first terminal window running to keep the tunnel alive . and type in the new terminal window : 

python3 -m http.server 8000

to test the server locally on your computer, open web browser and type : http://localhost:8000 
You should see a list of files and directories in the folder where you started the python3 -m http.server command.


to test the server from anywhere in the world : 
use the public url provided by ngrok on any device connected to the internet … type on your phone browser the public url:
example :

https://7b51-94-187-0-7.ngrok-free.app

and you will be able to browse all the file on your computer from anywhere !!!

or :

https://7b51-94-187-0-7.ngrok-free.app/index.html

will open the index.html from anywhere


If you want to keep the same URL each time you use ngrok: create a static domain on your dashboard and then use the --url flag to ask the ngrok agent to use it. First, stop ngrok with Ctrl+C and then run ngrok again with your static domain :

       ngrok http 8000 --url=terier-patent-monogoose.ngrok-free.app

if you want to add user and password :

 ngrok http http://localhost:8000 --basic-auth 'sam:Holyshit' --url=terier-patent-monogoose.ngrok-free.app

