# Celery and Flask App Builder -- P.O.C for Integration

To check integration:
1. Have redis up and running on port 6379. *(you can use docker and map the ports)*
   ```bash
    docker pull redis
    docker run -p 6379:6379 redis
   ```
2. Create a virtual environment:
   ```bash
    python3 -m venv env
    source env/bin/activate
   ````
3. Install requirements:
    ```bash
    pip3 install -r requirements.txt
    ```
4. Run celery worker:
    ```bash
    celery -A app.celery worker
    ```
5. Run the application:
    ```bash
    flask run
    ```
6. Go to any path which isn't defined in the app, let's say : http://localhost:5000/fasfdsafasfd