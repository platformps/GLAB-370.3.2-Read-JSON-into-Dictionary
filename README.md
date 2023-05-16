# GLAB-370.3.2-Read-JSON-into-Dictionary

## Lab Description
This lab focuses on reading JSON data into a dictionary in a Python program. It introduces learners to JSON (JavaScript Object Notation) and demonstrates how to extract data from a JSON file and store it in a dictionary for further processing. The lab provides hands-on experience with working with JSON data and dictionaries in Python.

## Learning Objectives
Understand the basics of JSON and its structure.
Learn how to read JSON data from a file.
Extract relevant data from the JSON file and store it in a dictionary.
Manipulate and access the data within the dictionary.
Apply the learned concepts to solve real-world scenarios.

## Prerequisites
Basic knowledge of Python programming.
Familiarity with data structures such as lists and dictionaries.

## Activities

### 1. Introduction to JSON
In this activity, you will gain an understanding of JSON and its usage in representing structured data. JSON is a lightweight data interchange format that is easy for humans to read and write. It is commonly used for transmitting data between a server and a web application, as well as for storing configuration settings and other data.

JSON consists of two main data structures: objects and arrays. Objects are enclosed in curly braces {}, while arrays are enclosed in square brackets []. Objects contain key-value pairs, where each key is a string and each value can be of any valid JSON type: string, number, boolean, null, object, or array.

Here's an example of a JSON object representing a person's information:

```
{
  "name": "John Doe",
  "age": 30,
  "city": "New York"
}
```

### 2. Reading JSON Data into a Dictionary

In this activity, you will learn how to read data from a JSON file and store it in a dictionary in Python. Python provides a built-in module called json that makes it easy to work with JSON data.

To read JSON data from a file, you need to follow these steps:

- [ ] Import the json module.
- [ ] Open the JSON file using the open() function.
- [ ] Load the contents of the file into a Python object using the json.load() function.
- [ ] Close the file.

Here's an example that demonstrates reading JSON data from a file named data.json:

```
import json

# Open the JSON file
with open('data.json') as file:
    # Load the JSON data into a Python object
    data = json.load(file)

# Print the data
print(data)
```

### 3. Accessing and Manipulating Data in the Dictionary

In this activity, you will learn how to access and manipulate data stored in a dictionary in Python. A dictionary is a collection of key-value pairs, where each key is unique. You can access the value associated with a key by using the key as an index.

To access a value in a dictionary, you can use the following syntax:

```
value = dictionary[key]
```

You can also modify the value associated with a key or add new key-value pairs to the dictionary using the same syntax.

Here's an example that demonstrates accessing and manipulating data in a dictionary:

```
# Create a dictionary
person = {
    "name": "John Doe",
    "age": 30,
    "city": "New York"
}

# Access a value
print(person["name"])  # Output: John Doe

# Modify a value
person["age"] = 31

# Add a new key-value pair
person["occupation"] = "Engineer"

# Print the updated dictionary
print(person)
```

### 4. Real-world Scenario: Analyzing JSON Data
In this activity, you will apply your knowledge of reading JSON data into a dictionary to solve a real-world scenario. Imagine you are working with a weather data provider, and you have been given a JSON file that contains weather information for different cities. Your task is to write a Python program that reads this JSON file, extracts relevant data, and performs specific operations on the extracted data.

Here are the steps to complete this activity:

- [ ] Open the JSON file using the open() function.
- [ ] Load the JSON data into a dictionary using the json.load() function.
- [ ] Extract the necessary data from the dictionary and perform the required operations. For example, you might want to calculate the average temperature across all cities or find the city with the highest rainfall.
- [ ] Generate the desired output based on the operations performed.
- [ ] Save and run your Python program to ensure it produces the correct output.
- [ ] Submit your completed Python program as part of your lab submission.


```
import json

# Open the JSON file
with open('weather_data.json') as file:
    # Load the JSON data into a Python object
    weather_data = json.load(file)

# Extract relevant data and perform operations
total_temperature = 0
max_rainfall = 0
rainy_cities = []

for city_data in weather_data:
    city_name = city_data['name']
    temperature = city_data['temperature']
    rainfall = city_data['rainfall']

    # Calculate the total temperature
    total_temperature += temperature

    # Find the city with the highest rainfall
    if rainfall > max_rainfall:
        max_rainfall = rainfall
        rainy_cities = [city_name]
    elif rainfall == max_rainfall:
        rainy_cities.append(city_name)
```

### Calculate the average temperature

```
average_temperature = total_temperature / len(weather_data)
```

### Generate the desired output

```
print("Average Temperature:", average_temperature)
print("City with Highest Rainfall:", ', '.join(rainy_cities))
```

In this example, we assume that the weather data is stored in a JSON file named weather_data.json, and each city's information is represented as a separate object within an array.

You should modify the code according to the actual structure of the JSON file and the specific operations you need to perform on the data.

## Lab Submission

As part of this lab, you are required to complete the real-world scenario mentioned in Activity 4. Write a Python program that reads the JSON data from the file, performs the necessary operations, and generates the expected output. Submit your completed Python program file with appropriate comments and any additional instructions, if required.

_Please ensure that your submitted program is well-documented and follows best practices for coding style and readability._
