<div align="center">

## Basics of PHP


</div>

### Description

This tutorial provides any beginner with the basic skills required to start programming in PHP.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[John Croucher](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/john-croucher.md)
**Level**          |Beginner
**User Rating**    |4.7 (70 globes from 15 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__8-1.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/john-croucher-basics-of-php__8-745/archive/master.zip)





### Source Code

<font color="#000000" face="Comic Sans MS" size="2">
<BR>PHP is a server side scripting language that makes it easy to create dynamic websites.
<BR>The code is similar to Java and C++ so if you know one or both of these languages you should be able to pick up PHP fairly easily.
<BR>
<BR>To use PHP you must either upload your site to a server that supports PHP or set up your own server. Unless you have a fast internet connection uploading your files for testing all the time will most likely not be a very good option for you. A good option is to have your own server on your local workstation. The best way to do this would be to use Windows 2000 or XP with Internet Information Services installed. You can then download the PHP engine and install it on your computer. This will allow you to test your pages quickly. However there are other ways of doing this such as the Apache sever.
<BR>
<BR>PHP is an embedded language. This means that you can embed code within a HTML document. There are a few ways in which this can be done:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;? echo ”Test Message”; ?&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This is the most common way of embedding code, but it may cause problems if your code must co-exist with XML.
<BR>
<BR>Another common way to embed is:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;?PHP echo ”Test Message”; ?&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>I recommend using this method for embedding for compatibility with other systems.
<BR>
<BR>There are two other alternate methods but these two aren’t used very often:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;% echo ”Test Message”; %&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>By default this method is turned off, and I do not recommend using it.
<BR>
<BR>The final way is similar to putting JavaScript in your page:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;SCRIPT LANGUAGE=”php”&gt;
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo ”TestMessage”;
<BR>&lt;/SCRIPT&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>Every file you create that contains PHP code you must make sure the extension is the PHP extension set on your server. I usually just use .php, but some people say that you should use the PHP version .php3 or .php4. I have never had any problems but there may be some issues with other servers which is why I still mentioned it.
<BR>
<BR>As I mentioned earlier PHP’s syntax comes from languages like C++. This means that you can use: // /* */ and even # for comments. Also the structure of things like for loops are similar, but variables in PHP are different.
<BR>All variables have a $ sign at the start and is followed by an alphabetic or underscore character. No data type declarations are necessary and you do not have to initialise the variables:
</FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;?
<BR>$name;
<BR>$name=”John”;
<BR>echo “My name is $name”;
<BR>?&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>OUTPUT:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;My name is John
<BR>
<BR>Notice how I can just put the variable name inside the output string.
<BR>Double quotes will be checked for variables and escape sequences.
<BR>If you do not want this to happen you would use single quotes:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>&lt;?
<BR>$name;
<BR>$name=”John”;
<BR>echo ‘My name is $name’;
<BR>?&gt;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>OUTPUT:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;My name is $name
<BR>
<BR>If you do wish to specify the data type for a variable you can use type casting:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>$number = (int) = “342asd”;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This will create an integer value of 342.
<BR>The types PHP supports are as follows:
<BR>
<BR>(int), (integer)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;– Cast to integer
<BR>(real), (double), (float)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;– Cast to float
<BR>(string)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;– Cast to string
<BR>(array)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Cast to array
<BR>(object)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Cast to object
<BR>
<BR>
<BR>Selection is something that is very important to know for every language. Selection in PHP is very similar to C++ and Java. We will fist start with the If statement:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if(expression){
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;statements
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This is a basic If statement. It is a bit hard to understand this way because we have nothing to test for so I will expand and put some sample data in.
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if($name == “John”){
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>Now with this data in it will say if the value in $name is equal to the string “John” then do the code within the braces.
<BR>We can then further expand on this to do something else if the value is not true:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if($name == “John”) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”;
<BR>} else {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “$name is not the creator of this tut”;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This code will do the same as previous but it will now output the second echo statement if it is not true.
<BR>Say the value of $name is “Bob”. It will go through and say is $name the same as “John”. No its not so we will go to else and output “Bob is not the creator of this tut”.
<BR>Getting confused? I hope not because we are going to expand on this code again and test for a second name.
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if($name == “John”){
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”;
<BR>} else if($name == “Bob”){
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “I don’t know any Bob”;
<BR>} else {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “$name is not the creator of this tut”;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This code again does the same as previous but it will test for two conditions.
<BR>Say the value of $name is still “Bob”. It will look at the first condition. Is the value in $name the same as “John”? No, So go to the next if. Is the value in $name the same as “Bob”? Yes, output “I don’t know any Bob”.
<BR>You can keep expanding on this testing for as many conditions as you wish.
<BR>
<BR>Just a note if you have only one line after you if statement you don’t have to have braces:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if($name == “John”)
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>But if you want two or more statements you must have braces. I just find it easier to use braces all the time.
<BR>
<BR>Also you may be wondering why I am using “==”. Well if you think to where you assign a value:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>$name = “John”;
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>That is how you assign a value, so if you had:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>if($name = “John”)
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>You would be trying to assign a value and you would receive an error.
<BR>Other comparisons you can do are things like &&, ||, >, <
<BR>I will explain the Boolean operators in a later tutorial.
<BR>
<BR>The next selection statement is the Switch. The basic syntax is as follows:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>switch(expression) {
<BR>case expression:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;statements
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>default:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;statements
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>Again this is a bit hard to follow so I will put some meaningful code in to help:
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>switch($name) {
<BR>case “John”:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>default:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;statements
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>This will basically do the same sort of thing as an if statement. If the value in $name is “John” then output “John is the creator of this tut”. If not then go to the next case, in this example the next case is the “default:”. This acts in a similar way to “else” in an if statement.
<BR>Also just like if statements you can expand and test for more values. To do this all you need to do is to add in more case statements.
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">
<BR>switch($name) {
<BR>case “John”:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “John is the creator of this tut”
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>case “Bob”:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;echo “I don’t know Bob”
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>default:
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;statements
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>That concludes my first PHP Tutorial.
Check out my <a href="http://www.jcroucher.com">site</a> for more tutorials and code.
<BR>
</Font>

