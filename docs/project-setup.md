# Project setup

Follow these steps from the project's root directory in your terminal.

**Note:** Following commands are particular to Linux OS.

1. Have Python >= 3.10 installed on your machine. Execute the following command to display Python version.

```
$ python3
```

2. Create Virtual Environment

```
$ python3 -m venv venv
```

3. Activate Virtual Environment

```
$ source venv/bin/activate
```

**Note:** If command is successful username on your terminal should get prefixed with **(venv)**

4. Install requirements of the project using the following command

```
$ pip3 install -r requirements.txt
```

5. Setup pre-commit

```
$ pre-commit install
```
