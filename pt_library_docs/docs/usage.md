# Documentation

### Notification
Sends a notification to the telegram channel.
```python
from pt_library import telegram_notification
response = telegram_notification(token, chat_id, message)

# response -> request.response
```

### Date-time
There are two functions, which return current date and previous month date.
```python
from pt_library import get_previous_month_year, get_current_month_year, get_timestamp
print(get_previous_month_year())
print(get_current_month_year())
print(get_timestamp())

# ('11', '2023') -> tuple(str)
# ('05', '12', '2023')->tuple(str)
# 2023-12-05 16:34:05->str
```

### SQL Queries
Executes SQL query and returns the result.
```python
from pt_library import run_query
result = run_query(host, user, password, database, query)
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