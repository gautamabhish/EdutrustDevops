# Edutrust DevOps

Welcome to the **Edutrust DevOps** project! This repository is your go-to resource for DevOps learning, experimentation, and project work related to the Edutrust application. We'll continuously update it with documentation, scripts, and other valuable resources as the project progresses.

---

## Getting Started

To get the Edutrust application running, choose your preferred deployment method below.

### 1. Local Development (using Docker)

Follow these steps to set up and run the application locally using Docker containers.

1.  **Prepare and Build the Docker Image:**

    First, clone the repository and then build the Docker image for the application.

    ```bash
    git clone [https://github.com/gautamabhish/Edutrust-Backend.git](https://github.com/gautamabhish/Edutrust-Backend.git)
    cd EdutrustDevops # Make sure this path is correct if your cloned repo structure differs.
    docker build -t edutrust-devops -f ./edutrustdevops/Dockerfile ./edutrust-backend
    ```

    *Note: The `.` at the end of your original command was likely causing issues with the build context. The corrected command specifies the build context as `./edutrust-backend`.*

2.  **Run the Docker container:**

    ```bash
    docker run --env-file=.env -d --name edutrust-devops-container -p 8080:5000 edutrust-devops
    ```

    This command runs the container in detached mode (`-d`), assigns it the name `edutrust-devops-container`, and maps port `8080` on your host to port `5000` inside the container.

3.  **Verify the application:**

    Open your web browser and navigate to `http://localhost:8080`.

    You should see an "Access denied" message, which indicates the application is running successfully.

### 2. Kubernetes Deployment (Coming Soon!)

This section will provide instructions for deploying the Edutrust application to a Kubernetes cluster. Stay tuned for updates!

---

## Contributing

We welcome your contributions! If you have suggestions for improvements, new scripts, or updated documentation, please feel free to [open an issue](https://github.com/gautamabhish/Edutrust-Backend/issues) or submit a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).

---