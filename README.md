# Battleship Online
Online multiplayer battleship board game made with socket and pygame

# Clips
![](screenshots/battleship.gif)
![](screenshots/gameover.png)

Running
-------
Server and client are Python packages with `__main__` entrypoints. From the project root run:

1) Create and activate a virtual environment (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

2) Start the server (defaults to listening on localhost:1234):

```powershell
python -m server
```

3) Start one or more clients (each client opens a pygame window):

```powershell
python -m client
```

To run the server on a different host/port (for LAN play), set environment variables before starting the server and matching values on the client:

PowerShell example:

```powershell
# start server listening on all interfaces port 2345
$env:SERVER_HOST = '0.0.0.0'; $env:SERVER_PORT = '2345'; python -m server

# on a client machine point to server's IP
$env:SERVER_HOST = '192.168.1.10'; $env:SERVER_PORT = '2345'; python -m client
```

Notes
-----
- Run `python -m client` from the project root so client can find assets under `client/assets`.
- If PowerShell blocks activation, run `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` for the session.
