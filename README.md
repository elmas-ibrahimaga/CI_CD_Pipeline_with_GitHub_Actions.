# **CI/CD Pipeline with GitHub Actions**

# **Project Overview**

This project demonstrates the creation and implementation of a CI/CD pipeline using GitHub Actions to automate:

Building a JAR file from a Java Spring Boot web application.

Uploading the JAR file to a cloud environment (AWS or Azure).

Creating and pushing a Docker image to DockerHub.

All tasks are triggered automatically upon a GitHub push or a pull request merge.

Our Postman [project](https://www.postman.com/iamkorniichuk/swe304/).

# **🚀 Key Objectives**
✅ Automate JAR file creation on GitHub.

✅ Automate Docker image creation and push to DockerHub.

✅ Automate cloud deployment (copying JAR to AWS/Azure).

✅ Use GitHub Secrets to securely manage DockerHub and cloud credentials.

✅ Demonstrate a complete DevOps pipeline.


## **🛠 Prerequisites**

Make sure you have the following installed on your system:

- **Java 17** ([Download](https://adoptium.net/))
- **Gradle** ([Install Guide](https://gradle.org/install/))
- **Docker** ([Download](https://www.docker.com/products/docker-desktop/))

## **📂 Installation**

1. **Clone the repository**

    ```bash
    git clone https://github.com/ipz215kvv/swe304-1.git
    cd swe304-1
    ```

2. **`.env` file**

    Create a `.env` file in the root directory and populate it with variables like shown in the [example](.env.example).

3. **Build `.jar` file**

    ```bash
    gradle clean build
    ```

4. **Build docker image**

    Firstly, start your docker service, then run:

    ```bash
    docker compose up --build
    ```

5. **Access the Web App**

    Once running, open your browser and go to:  
    👉 [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

    You will see the project scheme here.


## **🧳 Migrating from Maven to Gradle**

When you pull the commit replacing Maven with Gradle, follow these steps to migrate the project:

1. **Remove Maven-specific files**

   Delete the `pom.xml`, `mvnw`, `mvnw`, `mvnw.cmd` files, and `.mvn/` folder, as Gradle will no longer use it.

2. **Refresh dependencies**

    Your first build execution need to refresh newly added dependencies:

    ```bash
    gradle build --refresh-dependencies
    ```

# **📌 Final Notes**
This project showcases the ability to automate full-cycle application deployment. By integrating GitHub Actions with Docker and cloud services, we achieve a modern, efficient DevOps workflow—an essential skill for real-world software engineering.
