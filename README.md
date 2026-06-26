# Learn Flower (Celery Monitoring UI)

## Objective
The objective of this project is to learn how to use Flower, a web-based monitoring tool for Celery. Flower helps monitor Celery workers, tasks, queues, and task status in real time.

## Prerequisites
- Python 3.x
- Celery
- Redis
- Flower

## Installation

Install Flower using:

```bash
pip install flower
```

## Start Redis

```bash
redis-server
```

## Start the Celery Worker

```bash
celery -A tasks worker --loglevel=info
```

## Start Flower

```bash
celery -A tasks flower
```

## Open Flower Dashboard

Open your web browser and visit:

```
http://localhost:5555
```

## Sample Task

Example task in `tasks.py`:

```python
@app.task
def add(x, y):
    return x + y
```

Run the task:

```python
from tasks import add

result = add.delay(10, 20)
```

## Features
- Monitor Celery workers
- View active and completed tasks
- Monitor task queues
- View task status and results
- Web-based monitoring dashboard

## Output
- Flower dashboard launched successfully.
- Celery worker connected successfully.
- Tasks were executed and monitored in real time.

## Conclusion
Flower is a powerful monitoring tool for Celery that provides a user-friendly web interface to track workers, queues, and tasks. It simplifies debugging and monitoring of distributed task processing.