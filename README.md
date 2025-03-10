# Minitalk Project

Minitalk is a C project that implements communication between a client and a server using UNIX signals. This repository contains the source code for Minitalk, unit tests, and a CI pipeline with GitHub Actions.

## Project Structure

Here’s the project’s file structure:

.

├── .github/  
│   └── workflows/  
│   -    └── ci.yml  
├── exec/  
│   ├── client  
│   └── server  
├── tests/  
│   ├── bible.sh  
│   ├── bible.txt  
│   ├── tests.sh  
│   └── valgrind_tests.sh  
├── Makefile  
├── src  
├── README.md  



## Installation and Compilation

### Prerequisites

Ensure you have the following installed:

- A UNIX-based environment (Linux/macOS)
- `gcc` or `cc` compiler
- `make` for build management

### Installation Steps

1. Clone this repository:

    ```bash
    git clone https://github.com/Stafpecc/Minitalk_Tester.git minitalk && cd minitalk
    ```

2. Create an empty dir 'exec' 

    ```bash
    mkdir exec
    ```

4. Copy your code into minitalk, create a Malefile rule that compiles your cfiles into exec

5. Compile the executables `client` and `server`:

    ```bash
    make
    ```

6. After compilation, you should have the `client` and `server` executables inside the `exec/` directory.

## Running Tests

### Unit Tests

Unit tests are located in the `tests/` directory. You can run them using the following scripts:

- **`tests.sh`**: Basic client-server communication tests. (Execution time: < 1 min)
- **`bible.sh`**: A very very very very very very large test. (Execution time: long)

To run the tests, use:

```bash
./tests/tests.sh
./tests/bible.sh
```

### Running Valgrind Tests

Run the `valgrind_tests.sh` script to check the project’s memory management:

```bash
./tests/valgrind_tests.sh
```

---

### Explanation:
  
- **`tests` folder**: Contains scripts for unit tests (`tests.sh`), memory management tests using Valgrind (`valgrind_tests.sh`), very big test `bible.sh` and setup file bible test `bible.txt`.

- **`ci.yml`**: The GitHub Actions CI configuration file that automates compilation and test execution upon each push to the `main` branch.

- **Executables**: The `client` and `server` binaries are placed in the `exec/` directory after running `make`.

This setup provides a comprehensive, professional way to manage and run the project, along with automatic testing using GitHub Actions.
