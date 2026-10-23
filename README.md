# Experimental Constant Hash

A small Python web app for generating experimental 256-bit hashes. It uses only
the Python standard library.

## Run locally

```powershell
python server.py
```

Open <http://localhost:8000>.

## Deploy on Render

1. Push this project to a GitHub repository connected to your Render account.
2. In Render, create a **Blueprint** for that repository.
3. Set the Blueprint file path to `Desktop/files/render.yaml` (the project is
   in that subdirectory of the repository).
4. Apply the Blueprint and wait for the service to finish deploying.
5. Open the public URL shown on the Render service page.

The Blueprint builds the Python files, starts the web server, and checks
`/health`. Render assigns the `PORT` environment variable, which the server
already uses.

This is an experimental hash and has not been analyzed for cryptographic
security. Do not use it to protect passwords or sensitive data.
