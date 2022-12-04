java -jar -Dspring.profiles.active=prod -DFORUM_DATABASE_URL=jdbc:h2:mem:alura-forum -DFORUM_DATABASE_USERNAME=sa -DFORUM_DATABASE_PASSWORD= -DFORUM_JWT_SECRET=123456 forum.jar


docker run -p 8080:8080 -e SPRING_PROFILES_ACTIVE='prod' -e FORUM_DATABASE_URL='jdbc:mariadb://localhost:3308/alura-forum' -e FORUM_DATABASE_USERNAME='root' -e FORUM_DATABASE_PASSWORD='root' -e FORUM_JWT_SECRET='123456' alura/forum