# Python - Async Programming

## Overview
This project introduces asynchronous programming in Python using asyncio. It covers the async and await syntax, running asynchronous programs, executing concurrent coroutines, creating asyncio tasks, and using the random module. The goal is to understand how asynchronous execution improves performance when handling I/O-bound operations.

## Learning Objectives
By completing this project, I learned how to:
- Use async and await syntax
- Execute an async program with asyncio
- Run concurrent coroutines
- Create asyncio tasks
- Use the random module, including random.uniform
- Write type-annotated functions and coroutines
- Write clear documentation for modules and functions

## Requirements
- Ubuntu 20.04 LTS  
- Python 3.9  
- All files must end with a new line  
- The first line of all Python files must be:
#!/usr/bin/env python3
- Code must follow pycodestyle (version 2.5.x)  
- All files must be executable  
- File length will be tested using wc  
- All functions and coroutines must be type-annotated  

## Documentation Requirements
All modules and functions must include proper documentation. A valid documentation is a complete sentence explaining the purpose of the module or function and is not just a single word.

Examples to verify documentation:
python3 -c 'print(__import__("my_module").__doc__)'  
python3 -c 'print(__import__("my_module").my_function.__doc__)'  

## Example: Async Function
async def wait_random(max_delay: int) -> float:
    """Return a random delay after waiting asynchronously."""
    import random
    import asyncio
    delay = random.uniform(0, max_delay)
    await asyncio.sleep(delay)
    return delay

## Running an Async Program
python3 main.py

## Key Concepts
Async and Await: Used to define and manage asynchronous coroutines.  
Asyncio: A Python library used to run asynchronous programs and manage tasks.  
Concurrent Coroutines: Multiple coroutines can run concurrently using asyncio.gather or tasks.  
Random Module: Used to generate random values, such as delays in asynchronous examples.
