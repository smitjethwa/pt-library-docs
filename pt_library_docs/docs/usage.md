# Documentation

### Notification
Sends a notification to the telegram channel.
```python
from pt_library import telegram_notification
response = telegram_notification(token, chat_id, message)

# Params: token: str, chat_id: str, message:str 
# Return: response: requests.models.Response
```

### Date-time
There are two functions, which return current date and previous month date.
```python
from pt_library import get_previous_month_year, get_current_month_year, get_timestamp
print(get_previous_month_year())
print(get_current_month_year())
print(get_timestamp())

# {year: '2023',month: '11'}
# {year: '2023',month: '12', day: '05'}
# 2023-12-05 16:34:05       -> str
```

### SQL Queries
Executes SQL query and returns the result.
```python
from pt_library import run_query
result = run_query(host, user, password, database, query)

# Params: host: str, user: str, password:str, database:str, query:str 
# Return: tuple
```
### Decorators
###### Runtime calculation
Calculates the function execution time in minutes
```python
from pt_library import calculate_time

@calculate_time
def api_call():
    pass
```