.env file - Change address to reflect file name  MONGODB_URI = 'mongodb:/localhost/broken-dictionary'

changed name of package to broken-dictionary in package.json

.gitignore file - add .env

cahnge vars to const on www file (not necessary)

define mongoose in app.js

const Word = require('./routes/dictionary/models/Words'); doesnt need to go in app.js
Moved above path and changed the path for wordRoutes.js

Add the following to app.js = const wordRouter = require('./routes/dictionary/wordRoutes');

changed - mongoose.connect(process.env.MONGODB_URI)

changed - app.set view engine from jade to ejs

add the following middleware so the app can read the json 
app.use(express.json());
app.use(express.urlencoded({ extended: false }));


add module.exports to Words.js

add word should be router.post method

change post route to all lowercase addword

change delete path to have param :word