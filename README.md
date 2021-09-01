# Chocochip
This is my first repository that will be published to PyPI

## Goal 1: Publishing to PyPI
### Creating project structure
1. Clone the Github repository locally.
2. Create a subfolder with the same name as the package. We will refer this as primary subfolder.
3. Create a file named __init__.py inside the primary subfolder
4. Inside the primary subfolder create a python file with the same name as the package name.
5. Create a file named requirements_dev.txt

### Adding requirements
1. First of all identify the latest versions of pip and wheel and add them to the requirements_dev.txt
2. Now install it using `pip install -r requirements_dev.txt`

### Adding first function
1. Now add code to your main python file. In my case its `chocochip.py`
2. Here is my code snippet
```python
def give_me_a_cookie(name: str):
    """This function gives a cookie to the person who calls it

    Args:
        name (str): Name of the person

    Returns:
        str: Name of the person
    """
    print(f'Hi {name}! Here is your cookie again and again')
    return name
```