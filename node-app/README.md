    1  apt-get update
    2  apt-get install curl -y
    3  curl -sl https://deb.nodesource.com/setup_10.x | bash
    4  apt-get install nodejs -y
    6  cd opt
    8  mkdir node-app
    9  cd node-app
   11  echo 'console.log("nodejsapp from ubuntu")' > index.js
   13  index.js
   14  node index.js
   
