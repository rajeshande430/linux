# Input & Output Scripts
    ``
    #!/bin/bash
    name="Rajesh Ande"
    echo "Hello, My name is $name"
    read "username"
    echo "Hello, $username"
    ``
    ``
    #!/bin/bash
    count=100
    if [ $count -eq 100 ]
    then
    echo count is 100 2> /home/ubuntu/result.txt
    else
    echo count is not 100 > /home/ubuntu/result.txt
    fi
    ``
    ``
    #!/bin/bash
    if [ -e /home/ubuntu/result.txt ]
        then
        echo "file exist" 1> /home/ubuntu/result.txt
        else
        echo "file doesn't exist"
    fi
    ``
    #!/bin/bash
    echo "Hello, what is your name?"
    read name
    echo "Hello, $name"
    echo "do you like to work in IT?"
    read like
    if [ "$like" == yes ]
        then
        echo "Thats really cool"
        elif [ "$like" == no ]
        then
        echo "you should try out one $name"
    fi
# Case statements Scripts
    * if option a is selected = do this
    * if option b is selected = do this
    * if option c is selected = do this

```
#!/bin/bash
echo "Please choose one of the options below"
echo "a=Date and time"
echo "b=list home directory"
echo "c=who is logged in"
echo "d=systemuptime"
echo
read choices
echo
case $choices in
a) date;
b) ls /home/ubuntu;
c) who;
d) uptime;
*) echo Ohh no, its a invalid choice - bye
esac
```
# For Loop Scripts
* It keeps running untill a specified number of variable
    *   Example: variable = 10 then run the script for 10 times

```
#!/bin/bash
for i in 1 2 3 4 5
do
echo "welcome $i"
done
```
```
#!/bin/bash
for i in eating running jumping playing
do
echo "rajesh are you $i"
done
```
```
#!/bin/bash
name=Rajesh Ande
echo Welcome to play area $name
echo
echo Please choose one of the following options
for i in eating running playing
do
echo "what are you $i"
done
read choices
case $choices in
a) chicken
b) mutton
c) biryani
d) games
e) hockey
f) * invalid choice, Please choose CMBGH
esac
read answer
if [$answer = chicken]
then
echo chicken is a protein item
fi
```
