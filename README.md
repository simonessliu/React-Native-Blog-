# React-Native-Blog-

# To create a json server
1. the jsonserver folder can be found at: 
2. create a folder called jsonserver
3. into that folder we init a package.json by npm init -y
4. then we install json-server and ngrok from the command line
5. open the jsonserver in vscode
6. we create a file named db.json, and initialize the data 
7. in package.json we add 2 scripts with db: json-server -w db.json  and  tunnel : ngrok http 3000
8. run the following command in 2 seperate cmd, 1. npm run db and then npm run tunnel

ps: as we are using ngrok for free, as a result every 8 hours we need to update the url link 
![ngrok](https://user-images.githubusercontent.com/52482120/65219796-b1bbcf00-dafc-11e9-8ed9-2587014d8d12.png)


# To run this app
1. basically we need to open 3 terminals
2. one for npm run db and one for npm run tunnel and one for run expo start
3. simply clone this app and jsonserver app provide above and run npm -i for both of them and you are ready to go.

# For writing this app
initializing expo app by running: npx expo-cli init name, cd to that folder and run npm -i and then running expo start
installing react-navigation, we also need to install theses packages seperately

![install navigation up](https://user-images.githubusercontent.com/52482120/65219774-9f419580-dafc-11e9-87a4-de95cc00de80.png)

1. I use context to pass info among different components, and in order to make the context reuseable, also created an BlogContext file, so everytime we add a new action, we can pass that action to blogcontext 
2. using axios to fetch the data from the json server, to create axios, we put that 'dynamic' link(8hours) provided by ngrok which we can found on the cmd into axios file
3. so for each axios method like axios.get('/abc') the url inside the get() will be added after the ngork dynamic link 
4. the icon we are using is from expo vector icon, icon can be found at :
https://expo.github.io/vector-icons/, to use these icons we can just simply import { Feather } from '@expo/vector-icons' for example

