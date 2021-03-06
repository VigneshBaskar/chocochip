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
### Add setup.py file
Here is my template
```python
from setuptools import setup, find_packages

with open("README.md", "r") as readme_file:
    readme = readme_file.read()

setup(
    name="chocochip",
    version="0.0.1",
    author="Vignesh Baskaran",
    author_email="vignesh.sbaskaran@gmail.com",
    description="A package to provide you Chocochip cookies",
    long_description=readme,
    long_description_content_type="text/markdown",
    url="https://github.com/VigneshBaskar/chocochip",
    packages=find_packages(),
    classifiers=[
        "Programming Language :: Python :: 3.7",
        "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
    ],
)
```

### Install twine
1. Find the latest version of twine on PyPI
2. Add it to the requirements_dev.txt and install it using `pip install -r requirements_dev.txt`

### Commiting and Pushing the code to Github
1. Add and commit the modified files until now. In my case they are:
    1. README.md
    2. requirements_dev.txt
    3. chocochip/__init__.py
    4. chocochip/chocochip.py
    5. setup.py
2. Push the files to remote branch

### Publish on test PyPI
1. If you don't have a Test PyPI account, create one.
2. Then upload your package to Test PyPI using twine: `twine upload --repository-url https://test.pypi.org/legacy/ dist/*`
3. pip install -i https://test.pypi.org/simple/ --extra-index-url https://pypi.org/simple chocochip==0.0.1


## References:
1. https://towardsdatascience.com/build-your-first-open-source-python-project-53471c9942a7
2. https://stackoverflow.com/a/33685899/6882624
