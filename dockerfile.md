FROM eclipse-temurin:21-jdk
WORKDIR /app
COPY . /app
RUN javac -cp "web/lib/*" web/src/*.java
EXPOSE 8080
CMD java -cp "web/src:web/lib/*" Main