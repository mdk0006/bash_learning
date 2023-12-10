
# Shell Scripting

My Shell Scripting Learning

Shell Scripting Notes
---------------------
# Conventions
* Formatting 
* Following Name Conventions 
* Organizing and Structuring
Forementioned things make code readable,maintainable easier to work with
Includes --> variable,class,functions naming
## Variables 
user,user_address use underscores which is known as snake case 
For constants you can name in upper case letter
also `readonly` before name gives more visibility that the value should not be changed
variables that can be used by other scripts you can use export 
exort SOURCE_FILE 
## Functions 
* Always in the lower case and _ in between naming should be descriptive 
function_name() {
spacing and curly brace opening closing should be like this indentation of closing should be as start of function name
}
## Expanding Variables
How will be using the variable in the script 

```bash
  #!/bin/bash
  var="hi"
  echo ${var}
```
```bash
  #!/bin/bash
  var="hi"
  echo $var
```

but lets get another example
```bash
#!/bin/bash
height=170
echo "Your height=$heightcm"
```
will be getting error
```bash
#!/bin/bash
height=170
echo "Your height=${height}cm"
```
So surrounding the name of variable with curly braces is best practice but it can be overlooked for two cases
* Command Line Arguments
* Special Shell Variables
Also use double quotes to have right value of variable 
```bash
"${height}"
```
### Example
```bash
#!/bin/bash
string="one two three"
for element in string ${string};do
echo "${element}"
done
```
Output 
```
one
two
three
```
With Double Quotes
```bash
#!/bin/bash
string="one two three"
for element in string "${string}";do
echo "${element}"
done
```
In Conclusion use double quotes for 
* Filenames,Directory Paths
* Assigning URL to variables
* When in doubt use double quotes
*Note* $ sign can be used with other characters to expand variables
