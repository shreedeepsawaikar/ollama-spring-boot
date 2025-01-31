# Ollama Spring Boot Sample

This project demonstrates a simple Spring Boot application that interacts with an Ollama server.  It provides a basic example of how to send prompts to Ollama and receive responses within a Spring Boot environment.
This project uses deepseek-r1:1.5b model which can be swapped.

## Prerequisites

Before running this project, ensure you have the following installed:

* **Java:** Version 21 or higher is recommended.
* **Maven:** For dependency management.
* **Ollama:**  You'll need a running Ollama instance.  Follow the instructions on the [Ollama website](https://ollama.ai/) for installation and setup.  Make sure you have a model available that you want to use.
* **(Optional) Docker:** If you prefer to run Ollama in a Docker container, refer to the Ollama documentation for Docker instructions.

## Getting Started
git clone https://github.com/shreedeepsawaikar/ollama-spring-boot.git
cd ollama-spring-boot

ollama.base-url=http://localhost:11434  # URL of your Ollama server (default is http://localhost:11434)
ollama.model=llama2 # The name of the model you want to use

mvn clean install

mvn spring-boot:run


* **you can use below curl to verrify the respose.**
  
curl --location 'http://localhost:8080/api/ask' --no-buffer --header 'Content-Type: text/plain' --data 'quick sort in java'



