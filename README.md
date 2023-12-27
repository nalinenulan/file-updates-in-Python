# File Updates in Python

<h2>Description</h2>
Our company is trying to remove old IP addresses from our allowed list. In this project I will create a algorithm that can remove unwanted objects from a list. The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. In this project I show how to remove the unwanted IP addresses.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Atom</b> 

<h2>Program walk-through:</h2>

<p align="left">
Open the file that contains the allow list: <br/>
import_file= "allow_list.txt"<br />
with open(import_file, "r") as file:<br />

* In python we must import the file in order to use it within the algorithm. In this example I am saving it to the import_file name. In order to open the file we must use with  and open() as file: . With is used for reading or writing a file open is used to open() the file. then we have to pass the file import_file into the condition and specify that it is for reading using “r”
<br />
<br />

Read the file contents:<br />
import_file= "allow_list.txt" <br />
with open(import_file, "r") as file:<br />
&nbsp;&nbsp;&nbsp; ip_addresses = file.read()<br />
* To read the file in python we use . read() after the file which was named file. In this case we stored the read file under ip_addresses to make it easier to use later in the algorithm.
<br />
<br />

Convert the string into a list:<br/>
ip_addresses = ip_addresses.split()<br/>
* To make the file more useful we should make it into a list instead of a string. We can use the list to search every word/record in the file. By using .split() we can split the file between spaces. If we wanted to, we could insert a desired split object such as “,” or “.”. Since we did not specify the document defaults to spaces.
* We then save the new list back into the ip_adresses variable.
<br />
<br />

Iterate through the remove list:<br/>
for element in ip_addresses::<br/>

* To iterate through the list we must create a for loop. We then use a new variable called element and check if it is in the original list(ip_adresses) leading to for element in ip_adresses:
<br />
<br />

Remove IP addresses that are on the remove list:  <br/>
for element in ip_addresses:<br/>
&nbsp;&nbsp;&nbsp;if element in remove_list:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ip_addresses.remove(element)<br/>
* We must indent to show this is happening in the for loop. Then we create a conditional to see of the element is in the list we no longer want (remove_list) leading to if element in remove_list:
* We must indent to show this is happening in the if statement. Lastly, the conditional if is instructed to remove the element by using .remove() the code. The final line reads ip_addresses.remove(element)
<br />
<br />

Update the file with the revised list of IP addresses:<br/>
    ip_addresses = " ".join(ip_addresses)      
    with open(import_file, "w") as file:<br/>
&nbsp;&nbsp;&nbsp;file.write(ip_addresses)<br/>
* To update the file we must first rejoin the ip_adresses list into one string with .join(). We want to join it by adding a spce so we dont get just one long list of code and add “ ”. This all can be reflected in ip_addresses = " ".join(ip_addresses)  
* We must then open the original file (import_file) and say we are writing with “w” and temporarily save it as file.  You can see this on with open(import_file, "w") as file:
* Then, we must indent to show the file is open and the use .write() to edit a file. We then insert the updated file (ip_adresses) into the two (). All completed it looks like file.write(ip_addresses)
<br />
<br />

Summary:  <br/>
This code will remove any unwanted objects from a file. You can start by breaking down the overall task, instead of feeling overwhelmed just work through what you want the function to do. Then take steps until you are able to have a completed algorithm. I applied the
.remove() method to it to remove the element from ip_addresses. I used the
.join() method to convert the ip_addresses back into a string so that I could write over
the contents of the "allow_list.txt" file with the revised list of IP addresses.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
