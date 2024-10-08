Проект для изучения докер+java22+spring+hibernate+postgress+nginx

Build:
- ./mvnw package -s settings-home.xml
- java -jar target/demo-0.0.1-SNAPSHOT.jar
- docker build -t demoapp .
- docker run --rm -p 8081:8081 demoapp

Compile (sdk use java 21.0.4-tem):
- mvn clean -s settings-home.xml
- mvn compile -s settings-home.xml
- mvn test -s settings-home.xml

План:
1. Подрубить контейнер с базой, внести зависимости для работы с базой
2. Реализовать crud для юзера (рестами)
4. Усложнить логику, добавить больше сущностей и логики
5. Поменять веб-сервер на nginx (сейчас поднимается на tomcat)
6. Запустить базу без orm, пульнуть прямые запросы, поработать с соединенями

Глобально по проектам:
1. База - докер+java22+spring+hibernate+postgress+nginx
2. Углубиться в спринг, hibernate
2. Многопоточность, высоконагруженные проекты
4. kuber?