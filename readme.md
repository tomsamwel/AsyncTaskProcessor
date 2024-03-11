# Async Task Processor

The Async Task Processor is a lightweight, easy-to-use Python library designed to manage and process asynchronous tasks efficiently. Utilizing Python's asyncio library, it offers a straightforward way to queue tasks, process them asynchronously, and retrieve their statuses and results.

## Features

- Simple task queue management.
- Asynchronous processing of tasks with real-time status updates.
- Flexible task creation supporting any callable Python function.
- Comprehensive task status tracking, from queued to completed or failed.

## Installation

Install async_task_processor using pip:

```bash
pip install async_task_processor
```

## Quick Start

To get started with Async Task Processor, follow these steps:

1. **Create a Task**

```python
from async_task_processor.models import Task

# Define your asynchronous function
async def sample_task_function(arg1, arg2):
    # Your async task logic here
    return arg1 + arg2

# Create a task
task = Task(task_id="1", function=sample_task_function, args=[10, 20])
```

2. **Initialize the Processor and Add Tasks**

```python
from async_task_processor.async_task_processor import AsyncTaskProcessor

processor = AsyncTaskProcessor()

# Add tasks to the processor
await processor.add_task(task)
```

3. **Process the Tasks**

```python
# Start processing tasks
await processor.process_tasks()
```

## Contribute

Contributions are welcome! If you have a feature request, bug report, or a pull request, please open an issue or submit a pull request.
