# spotik-config-service

<h3>Welcome to the Spotik config service</h3>
Here you should configure how properties will be shared:


/application.yml
``` yml
        git:
          uri: ${uri_to_folder}
          username: ${git_username}
          password: ${git_token}
```

in this repository from URI, there should be two configuration files: 
</br>
/spotik_service.yml
``` yml
spotify:
  id: ${spotify_project_id}
  secret: ${spotify_project_secret}
  uri: http://localhost:8080
db:
  url: jdbc:postgresql://localhost:5432/postgres
  user: ${db_username}
  password: ${db_password}
  driver: org.postgresql.Driver
  dialect: org.hibernate.dialect.PostgreSQLDialect
spring:
  rabbitmq:
    host: localhost
    port: 5672
    username: ${rabbitmq_username}
    password: ${rabbitmq_password}
rabbitmq:
  queue: last_releases
  exchange: last_releases_exchange
  routing_key: last_releases_routing_key
```

/spotik_telegram_service.yml
```yml
telegram:
  bot:
    username: ${your_bot_name}
    token: ${telegram_bot_token}
rabbitmq:
  queue: last_releases
mail:
  username: ${mail}
  password: ${secret_from_mail}
db:
  url: jdbc:postgresql://localhost:5432/postgres
  user: ${db_username}
  password: ${db_password}
  driver: org.postgresql.Driver
  dialect: org.hibernate.dialect.PostgreSQLDialect
```

<h2>Quick Start</h2>
To get the project off to a good start, you need to start each service in the right direction:
<ol>
<li> <strong>spotik-config-service</strong> -> https://github.com/nhavronskyi/spotik-config-service</li>
<li> <strong>spotik-service</strong> -> https://github.com/nhavronskyi/spotik-service</li>
<li> <strong>spotik-telegram-service</strong>strong> -> https://github.com/nhavronskyi/spotik-telegram-service</li>
</ol>
