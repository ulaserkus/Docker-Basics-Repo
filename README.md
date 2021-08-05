**Docker** 

-version bilgisi
docker version 

-image çekme
docker pull  …….
Ex:docker pull mongo

-image çalıştırma
docker run  ……..
Ex:docker run mongo
Eğer image yoksa kurulumunu da yapar

-imageleri listler
docker images

-isim üzerinden ilerlenirse başlatma ve durdurma işlemleri
docker start ..NAME..
docker stop ..NAME..

-çalışan process listesi
docker ps

-geçmişe yönelik çalışan process listesi
docker ps -a

-container silme işlemi 
docker rm ..NAME..

-containerların tamamını silmek için
 docker container rm $(docker container ls -aq)

-docker port mapping için
Öncelikle docker hosta ulaşmamız gerekir
docker run -p DIS_PORT:IC_PORT mongo

-bağlantı için  - -link  detach başlatma -d  
docker run --name pmyadmin -p 8000:80 --link mysql-server:db  -d  phpmyadmin/phpmyadmin

-server işlemleri -e environment variable tanımlama -v volume mapping kayıt altına almak için kullanılır  - -name isim verir
docker run --name mysql-server -p 3306:3306 -e MYSQL_ROOT_PASSWORD=test123 -v /opt/data:/etc/mysql/conf.d -d  mysql

-network oluşturma işlemi
docker network create --driver bridge --subnet 182.18.0.1/24 --gateway 182.18.0.1 custom-network

-docker image oluşturma için
docker build . -t ..APPNAME..

-.dockerignore dosyası .gitignore ile aynı işlevi görmektedir.İçeriği aşağıdaki gibidir istenmeyen klasörler eklenmez.
node_modules/

-docker-compose farklı servisleri birlikte build almayı ve çalıştırmayı sağlar
Dosya adı docker-compose.yml ‘ dir.
                
docker-compose up hem build alır hem çalıştırır
docker-compose build sadece derleme yapar
