# tempt
tempt is a flexible and powerful Python template engine designed to make it easy to substitute placeholders in templates with actual values. With its simple syntax, tempt allows developers to create dynamic and customizable templates for web applications. This document will cover the features of tempt, how to use it, and how to contribute to the project.

### Features:

* Templating: tempt provides basic template functionality, including variable substitution, template inheritance, includes, control structures, and filters.
* Simple syntax: The syntax used by tempt is simple, using double curly braces (e.g. {{ variable }}) for placeholders and special syntax (e.g. {% if condition %} ... {% endif %}) for control structures.
* Inheritance: tempt supports template inheritance, allowing developers to create a base template with common elements and then extend it with more specific templates.
* Customizable: tempt is highly extensible, allowing developers to add their own filters and control structures as needed.

### Get started:

1. First, create an HTML template file, e.g., template.html:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile</title>
</head>
<body>
    <h1>Hello, {{ name }}!</h1>
    {% if show_age %}
    <p>You are {{ age }} years old.</p>
    {% endif %}
</body>
</html>
```

2. Next, write a Python script to use the tempt framework:

```
import re

# Include the `tempt` class here

def main():
    # Instantiate the `tempt` engine with the template file path
    engine = tempt("template.html")

    # Define the context (data) to be used for substitution
    context = {
        "name": "Darth Vader",
        "age": 44,
        "show_age": True
    }

    # Render the template with the context data
    output = engine.render(context)

    # Print the rendered output
    print(output)

if __name__ == "__main__":
    main()
```


3. When you run the script, the tempt framework will render the template file template.html with the provided context data and produce the following output:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile</title>
</head>
<body>
    <h1>Hello, Darth Vader!</h1>
    <p>You are 44 years old.</p>
</body>
</html>
```

### PYPI
https://pypi.org/project/tempt/.

### Contributing:
tempt is an open-source project and contributions are welcome!
