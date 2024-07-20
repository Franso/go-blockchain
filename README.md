# Go Blockchain

A simple blockchain implementation in Go.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project is a basic implementation of a blockchain in Go. It includes functionalities to create blocks, validate them, and serve the blockchain over HTTP.

## Features

- Create and validate blocks
- Serve the blockchain over HTTP
- Simple and easy-to-understand codebase

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Franso/go-blockchain.git
    cd go-blockchain
    ```

2. Install dependencies:
    ```sh
    go mod tidy
    ```

3. Create a `.env` file in the root directory and set the `PORT` environment variable:
    ```sh
    echo "PORT=8080" > .env
    ```

## Usage

1. Run the application:
    ```sh
    go run main.go
    ```

2. The server will start and listen on the port specified in the `.env` file (default is 8080).

## API Endpoints

### Get Blockchain

- **URL:** `/`
- **Method:** `GET`
- **Success Response:**
    - **Code:** 200
    - **Content:** JSON array of blocks

### Add Block

- **URL:** `/`
- **Method:** `POST`
- **Data Params:**
    - **Content-Type:** `application/json`
    - **Body:** 
        ```json
        {
            "Data": 123
        }
        ```
- **Success Response:**
    - **Code:** 201
    - **Content:** JSON object of the new block

