# Git 101

## Git filter

To implement the filter modify the local project file `.git/config` to add the filter:

```properties
[filter "nameFilter"]
  clean = sed -e 's|My name is: <MY_NAME>|My name is: <MY_NAME>|g' -e 's|My surname is: <MY_SURNAME>|My surname is: <MY_SURNAME>|g' 
  smudge = sed -e 's|My name is: <MY_NAME>|My name is: <MY_NAME>|g' -e 's|My surname is: <MY_SURNAME>|My name is: Cabrerizo|g'
```

Replacing "Juan" and "Cabrerizo" with your name *in both lines*. This example uses the pipe character as delimitator on the `sed` command

Also addging an entry y the `.gitattribbutes` file in the root of the project is needed, maping each file to be analyzed by the filter with the filter name added to the config file:

```properties
README.md filter=nameFilter
```

My name is: <MY_NAME>

My surname is: <MY_SURNAME>
