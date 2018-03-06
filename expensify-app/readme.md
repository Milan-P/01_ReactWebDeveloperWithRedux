# BASE

npm install -g live-server
live-server public																první okno nechat běžet
yarn init																		odpovedi na otázky
yarn add babel-preset-react babel-preset-env
babel src/app.js --out-file=public/scripts/app.js --presets=env,react
babel src/app.js --out-file=public/scripts/app.js --presets=env,react --watch	druhé okno nechat běžet
(npm uninstall -g babel-cli live-server)										v případě, že je potřeba něco odinstalovat globálně
yarn add live-server babel-cli
(yarn run serve)																v případě startu scriptu z package.json
yarn add webpack
(zastavit --watch)
(webpack.js.org)																stránky webpack
(node webpack.config.js)														spustí webpack.config.js
(nodejs.org/api/path.html)														node documentation
yarn run build																	okno nechat běžet (vytvoří bundle.js)
(npmjs.com/package/validator)													
yarn add validator
yarn add react react-dom														+react +react-dom
yarn add babel-core
yarn add babel-loader
yarn add webpack-dev-server
yarn run dev-server
yarn add babel-plugin-transform-class-properties
yarn add react-modal

# Servers

live-server public
yarn run dev-server
yarn run build

yarn add style-loader css-loader
yarn add sass-loader node-sass
yarn add normalize.css

# React Router

yarn add react-router-dom@4.2.2
yarn add redux@3.7.2
(npm config set python C:\APP\ReactNative\Setups\Python27\python.exe)
yarn add uuid
yarn add babel-plugin-transform-object-rest-spread
yarn add react-redux

;;;yarn add moment react-dates react-addons-shallow-compare
yarn add moment@2.18.1 react-dates@12.7.0 react-addons-shallow-compare@15.6.0
(http://momentjs.com/)

;;;install chrome and install google:"redux developer tools extension"
;;;https://facebook.github.io/jest/
yarn add jest@20.0.4
(yarn test)
;;; yarn test -- --watch
yarn add react-test-renderer@16.0.0
;;;styling od  Reset That $#!*

yarn add enzyme@3.0.0 enzyme-adapter-react-16@1.0.0 raf@3.3.2
(http://airbnb.io/enzyme/)
yarn add enzyme-to-json@3.0.1

# Git Commands

(git --version)
git init
git status
(.gitignore)
git add package.json
git add .

git config --global user.email "milan.pilar@lti.cz"
git config --global user.name "Milan Pilar"
git commit -m "Initial commit"
git log

https://help.github.com/articles/connecting-to-github-with-ssh/
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows
ssh-keygen -t rsa -b 4096 -C "milan.pilar@lti.cz"
výstup do: C:\Program Files\OpenVPN\easy-rsa\.ssh

ls -a ~/.ssh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
pbcopy < ~/.ssh/id_rsa.pub
ssh -T git@github.com

git remote add origin https://github.com/Milan-P/react-course-2-expensify-app.git
git remote							(odpověď origin)
git remote -v
git push -u origin master
git status

ssh-keygen -t rsa -b 4096 -C "milan.pilar@lti.cy" 
;git remote add origin https://github.com/Milan-P/react-course-2-indecision-app.git
;git push -u origin master

# Build

yarn run build:dev
yarn run build:prod

yarn add extract-text-webpack-plugin@3.0.0

git status
git add .
git commit -m "Setup production webpack build"
git push

(expressjs.com - pro node.js)
yarn add express@4.15.4
(pro otestování: node server/server.js)

# Heroku

(heroku.com - instalace heroku-cli-x64.exe)
heroku --version
heroku login
heroku create react-course-2-788-expensify
git remote
git remote -v
git push heroku master
heroku open
heroku logs
https://react-course-2-788-expensify.herokuapp.com/

*/
yarn install
git add yarn.lock
git commit -m "Updated Yarn lockfile"
git push heroku master
/*

yarn add chalk --dev
yarn install --production

(numeraljs.com)
yarn add numeral@2.0.6

# Firebase

const config = {
  apiKey: "AIzaSyDwLR61x74Kc4n3ggHbD0ppzxsO9-vSVhc",
    authDomain: "expensify-8888f.firebaseapp.com",
    databaseURL: "https://expensify-8888f.firebaseio.com",
    projectId: "expensify-8888f",
    storageBucket: "expensify-8888f.appspot.com",
    messagingSenderId: "358603088719"
};

;DEV
FIREBASE_API_KEY=AIzaSyDwLR61x74Kc4n3ggHbD0ppzxsO9-vSVhc
FIREBASE_AUTH_DOMAIN=expensify-8888f.firebaseapp.com
FIREBASE_DATABASE_URL=https://expensify-8888f.firebaseio.com
FIREBASE_PROJECT_ID=expensify-8888f
FIREBASE_STORAGE_BUCKET=expensify-8888f.appspot.com
FIREBASE_MESSAGING_SENDER_ID=358603088719

;TEST
FIREBASE_API_KEY=AIzaSyBOdWVtbI-oZqwR8X3Ol3UGCBQACPe3RK0
FIREBASE_AUTH_DOMAIN=expensify-test-c57c5.firebaseapp.com
FIREBASE_DATABASE_URL=https://expensify-test-c57c5.firebaseio.com
FIREBASE_PROJECT_ID=expensify-test-c57c5
FIREBASE_STORAGE_BUCKET=expensify-test-c57c5.appspot.com
FIREBASE_MESSAGING_SENDER_ID=524349000752


yarn add firebase@4.2.0
yarn add redux-thunk@2.2.0
yarn add redux-mock-store@1.2.3
yarn add --dev cross-env@5.0.5
yarn add --dev dotenv@4.0.0			(--dev = for development purposes only)

# Heroku

heroku config
heroku config:set KEY=value
heroku config
heroku config:unset KEY
heroku config
heroku config:set FIREBASE_API_KEY=AIzaSyDwLR61x74Kc4n3ggHbD0ppzxsO9-vSVhc 
heroku config:set FIREBASE_AUTH_DOMAIN=expensify-8888f.firebaseapp.com
heroku config:set FIREBASE_DATABASE_URL=https://expensify-8888f.firebaseio.com
heroku config:set FIREBASE_PROJECT_ID=expensify-8888f
heroku config:set FIREBASE_STORAGE_BUCKET=expensify-8888f.appspot.com
heroku config:set FIREBASE_MESSAGING_SENDER_ID=358603088719

git status
git add .
git commit -m "T1"
git push
git push heroku master

yarn run dev-server
yarn add history@4.7.2

# Firebase Rules

{
  "rules": {
    ".read": false,
    ".write": false,
    "users": {
      "$user_id": {
        ".read": "$user_id === auth.uid",
        ".write": "$user_id === auth.uid",
        "expenses": {
          "$expense_id": {
            ".validate": "newData.hasChildren(['description', 'note', 'createdAt', 'amount'])",
            "description": { 
            	".validate": "newData.isString() && newData.val().length > 0"
            },
            "note": { 
            	".validate": "newData.isString()"
            },
            "createdAt": { 
            	".validate": "newData.isNumber()"
            },
            "amount": { 
            	".validate": "newData.isNumber()"
            },
            "$other": {
              ".validate": false
            }
          }
        },
        "$other": {
          ".validate": false
        }
      }
    }
  }
}

{
	"description": "Rent",
	"note": "",
	"amount": 0,
	"createdAt": 0
}

# Finalization

yarn add babel-polyfill@6.26.0
yarn test -- --watch

;15->16 version

