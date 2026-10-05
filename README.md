# Task 3: Terraform and Docker

This project uses Terraform with the Docker provider to create an Nginx container named `terraform-nginx`. It maps port `8080` on your computer to port `80` in the container.

## Prerequisites

- Terraform 1.5 or later
- Docker installed and running

## Run the project

Open a terminal in this project folder, then run:

```sh
terraform init
terraform validate
terraform plan
terraform apply
```

Type `yes` when Terraform asks you to confirm the apply. Docker downloads the Nginx image if it is not already available locally.

## Verify Nginx

Open [http://localhost:8080](http://localhost:8080) in a browser. You should see the Nginx welcome page.

To inspect Terraform's tracked resources, run:

```sh
terraform state list
```

## Clean up

Remove the container managed by this project with:

```sh
terraform destroy
```

Type `yes` to confirm. Because `keep_locally` is enabled, Terraform leaves the downloaded Nginx image in Docker after destroying the container.

## Push to GitHub

Create or open your GitHub repository named `terraform`, then upload these three files to its root: `main.tf`, `README.md`, and `.gitignore`.
