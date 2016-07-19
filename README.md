# jenkins-docker-slaves
These are Dockerfiles for creating Jenkins slaves for NDN-RTC CI

## How to use
1. In Jenkins, create slave node and choose "Launch slave agents via Java Web Start"
2. Jenkins should give you a command to launch headless slave, something like this:

    ````
    java -jar slave.jar -jnlpUrl <jnlp_url> -secret <secret>
    ````


3. Use `jnlpUrl` and `secret` arguments as environment variables to run image:

    ```
    docker run -e JNLP_URL="<jnlp_url>" -e SECRET="<secret>" peetonn/jenkins-docker-slaves:ubuntu12.04
    ```
