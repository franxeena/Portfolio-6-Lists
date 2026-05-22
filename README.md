# Portfolio 6: Lists
## Title: Sleep Tracker Program
### This program records the user's sleep hours
### for several days using Python lists.

### The program will:
#### - Store sleep hours in a list
#### - Calculate average sleep
#### - Find highest and lowest sleep hours
#### - Check if a specific sleep hour exists
#### - Use loops, conditions, indexing, and split()

### Create an empty list
```python
sleep_hours = []
print("Weekly Sleep Tracker")
```
### Ask the user for sleep hours
```python
while True:
```
#### User input
```python
    inp = input("Enter hours of sleep or type 'done': ")
```
#### Stop the loop
```python
    if inp == 'done':
        break
```
#### Convert input to float
```python
    hours = float(inp)
```
#### Add value to the list
```python
    sleep_hours.append(hours)
```
### Display the complete list
```python
print("Recorded Sleep Hours:")
print(sleep_hours)
```
### Make sure list is not empty
```python
if len(sleep_hours) > 0:
```
#### Calculate average sleep
```python
    average_sleep = sum(sleep_hours) / len(sleep_hours)
```
#### Display statistics
```python
    print("Sleep Statistics")
    print("Days Recorded:", len(sleep_hours))
    print("Highest Sleep Hours:", max(sleep_hours))
    print("Lowest Sleep Hours:", min(sleep_hours))
    print("Average Sleep Hours:", average_sleep)
```
### Check if user slept exactly a certain amount
```python
search = float(input("Enter sleep hours to search: "))
```
### Membership checking
```python
if search in sleep_hours:
    print("You slept that amount on one of the days!")
else:
    print("That sleep hour was not recorded.")
```

### BONUS PART: Using split()

```python
print("Sleep Notes")
```
### Ask user for sleep moods
```python
notes = input("Enter sleep moods separated by spaces: ")
```
### Convert string into list
```python
mood_list = notes.split()
```
### Display moods
```python
print("Sleep Moods:")
for mood in mood_list:
    print(mood)
```
### Display first mood using indexing
```python
if len(mood_list) > 0:
    print("First mood entered:", mood_list[0])

print("Sleep tracking completed.")
```