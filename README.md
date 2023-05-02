Download Link: https://assignmentchef.com/product/solved-comp1210-project-8-dodecahedron-list2-menu-app
<br>
<strong>Deliverables </strong>

Your project files should be submitted to Web-CAT by the due date and time specified.  You may submit your files to the <u>skeleton code</u> assignment until the project due date but should try to do this by Friday (there is no late penalty since the skeleton code assignment is ungraded for this project).  The files you submit to skeleton code assignment may be incomplete in the sense that method bodies have at least a return statement if applicable or they may be essentially completed files.  In order to avoid a late penalty for the project, you must submit your <u>completed code</u> files to Web-CAT no later than 11:59 PM on the due date for the completed code.  You may submit your <u>completed code</u> up to 24 hours after the due date, but there is a late penalty of 15 points.  No projects will be accepted after the one-day late period.  If you are unable to submit via Web-CAT, you should e-mail your project Java files in a zip file to your TA before the deadline.




<strong>Files to submit to Web-CAT</strong> (all three files must be submitted together):<strong>   </strong>

<ul>

 <li>java</li>

 <li>java</li>

 <li>java</li>

</ul>




<strong>Specifications – </strong><strong>Use arrays in this project; ArrayLists are not allowed!</strong><strong>   </strong>

<strong>Overview: </strong><u>The objective is to modify your Project 6 to use arrays instead of ArrayList objects</u>.  You will write a program this week that is composed of three classes: the first class defines Dodecahedron objects, the second class defines DodecahedronList2 objects, and the third,

DodecahedronList2MenuApp, presents a menu to the user with eight options and implements these:

(1) read input file (which creates a DodecahedronList2 object), (2) print report, (3) print summary, (4) add a Dodecahedron object to the DodecahedronList2 object, (5) delete a Dodecahedron object from the DodecahedronList2 object, (6) find a Dodecahedron object in the DodecahedronList2 object, (7) Edit a Dodecahedron in the DodecahedronList2 object, and (8) quit the program.<strong> [You should create a new “Project 8” folder and copy your Project 6 files </strong>(Dodecahedron.java,

DodecahedronList.java, DodecahedronListMenuApp.java, dodecahedron_data_1.txt, and dodecahedron_data_0.txt)<strong> to it, rather than work in the same folder as Project 6 files.]  </strong>

<strong> </strong>

<strong><u>To rename an existing .java file, </u>open the file in jGRASP, change the name of the class and the name of the constructor (if it has one) in the source file, and then click the Save button.  In the dialog that pops up, click the “Rename and Save” button.  This will rename save the .java file and delete the old associated .class file. </strong>




<ul>

 <li><strong>Dodecahedron.java (<u>assuming that you successfully created this class in Project 4, 5, or 6</u> <u>just copy the file to your new Project 8 folder and go on to DodecahedronList2.java on page</u> </strong></li>

</ul>

<ol start="4">

 <li><strong><u> Otherwise, you will need to create Dodecahedron.java as part of this project</u>.) </strong></li>

</ol>

<strong> </strong>

<strong>Requirements</strong>: Create a Dodecahedron class that stores the label, color, and edge (i.e., length of an edge, which must be greater than zero).  The Dodecahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of a Dodecahedron object, and a method to provide a String value of a Dodecahedron object (i.e., a class instance).

<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">A dodecahedron has 12 equal pentagonal faces, 20 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective Dodecahedron methods described in this project.</td>

  </tr>

  <tr>

   <td width="198"> </td>

   <td width="184"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204">    </td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>

<strong>       </strong>

<strong>Design</strong>:  The Dodecahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Dodecahedron class, and <u>these should be the only instance variables in the class</u>.</li>

</ul>




<ul>

 <li><strong>Constructor</strong>: Your Dodecahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Dodecahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>




Dodecahedron example1 = new Dodecahedron(“Small Example”, “blue”, 0.25);




Dodecahedron example2 = new Dodecahedron(” Medium Example “, “orange”, 10.1);




Dodecahedron example3 = new Dodecahedron(“Large Example”, “silver  “, 200.5);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Dodecahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.</li>

 <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

 <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

 <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

 <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

 <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.</li>

 <li>surfaceArea: Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

 <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

 <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

 <li>toString: Returns a String (does<u> not </u>begin with 
) containing the information about the Dodecahedron object formatted as shown below, including decimal formatting (“#,##0.0##”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method: surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).</li>

</ul>




Dodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.    surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777




Dodecahedron “Medium Example” is “orange” with 30 edges of length 10.1 units.

surface area = 2,106.071 square units    volume = 7,895.319 cubic units    surface/volume ratio = 0.267




Dodecahedron “Large Example” is “silver” with 30 edges of length 200.5 units.    surface area = 829,963.459 square units    volume = 61,765,889.248 cubic units    surface/volume ratio = 0.013




<strong>Code and Test</strong>: As you implement your Dodecahedron class, you should compile it and then test it using interactions.  For example, as soon you have implemented and successfully compiled the constructor, you should create instances of Dodecahedron in interactions (e.g., copy/paste the examples above).  Remember that when you have an instance on the workbench, you can unfold it to see its values.  You can also open a viewer canvas window and drag the instance from the Workbench tab to the canvas window.  After you have implemented and compiled one or more methods, create a Dodecahedron object in interactions and invoke each of your methods on the object to make sure the methods are working as intended.  You may find it useful to create a separate class with a main method that creates an instance of Dodecahedron then prints it out.




<ul>

 <li><strong>DodecahedronList2.java – You must use arrays instead of ArrayList objects. (<u>Assuming</u> <u>that you successfully created this class in Project 6, just copy DodecahedronList.java to</u> <u>your new Project 8 folder and then open in jGRASP and rename as DodecahedronList2.</u>  <u>To rename an existing .java file, open the file in jGRASP, change the name of the class and</u> <u>the name of the constructor in the source code, and then click the Save button.  In the dialog</u> <u>that pops up, click the “Rename and Save” button.  This will rename and save the .java file</u> </strong></li>

</ul>

<strong><u>and then delete old associated .class file.  Otherwise, you will need to create all of</u> </strong>

<strong><u>DodecahedronList2.java as part of this project</u>.)  In the requirements below, </strong>

<strong><u>DodecahedronList has been changed to DodecahedronList2. Be sure to make these changes</u> <u>in your methods as necessary.</u></strong>




<strong>Requirements</strong>: Create a DodecahedronList2 class that stores the name of the list and an array of Dodecahedron objects.  It also includes methods that return the name of the list, number of Dodecahedron objects in the DodecahedronList2, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Dodecahedron objects in the DodecahedronList2.  The toString method returns a String containing the name of the list followed by each Dodecahedron in the array, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The DodecahedronList2 class has <u>three fields</u>, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list, (2) an array of Dodecahedron objects, and (3) an int representing the number of elements in the array of Dodecahedron objects. These are the only fields (or instance variables) that this class should have.</li>

 <li><strong>Constructor</strong>: Your DodecahedronList2 class must contain a constructor that accepts a parameter of type String representing the name of the list, a parameter of type</li>

</ul>

Dodecahedron[], representing the list of Dodecahedron objects, and a parameter of type int representing the number of elements in the Dodecahedron array.  These parameters should be used to assign the fields described above (i.e., the instance variables).

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for DodecahedronList2 are described below.

  <ul>

   <li>getName: Returns a String representing the name of the list.</li>

   <li>numberOfDodecahedrons: Returns an int representing the number of</li>

  </ul></li>

</ul>

Dodecahedron objects in the DodecahedronList2.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>totalSurfaceArea: Returns a double representing the total surface areas for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalVolume: Returns a double representing the total volumes for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceArea: Returns a double representing the average surface area for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageVolume: Returns a double representing the average volume for all</li>

</ul>

Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Dodecahedron in the list.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method for each Dodecahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from DodecahedronList2App for the <em>txt</em> input file. [<u>Note that the toString result should <strong>not</strong> include the return value of summaryInfo()</u>.]</li>

 <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Dodecahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.</li>

 <li>getList: Returns the array of Dodecahedron objects (the second field above).</li>

 <li>readFile: Takes a String parameter representing the file name, reads in the file, storing the list name and creating an array of Dodecahedron objects, uses the list name, the array, and number of Dodecahedron objects in the array to create a</li>

</ul>

DodecahedronList2 object, and then returns the DodecahedronList2 object.  See note #1 under <u>Important Considerations</u> for the DodecahedronList2MenuApp class (last page) to see how this method should be called. <strong> </strong>

<ul>

 <li>addDodecahedron: Returns nothing but takes three parameters (label, color, and edge), creates a new Dodecahedron object, and adds it to the DodecahedronList2 object.</li>

 <li>findDodecahedron: Takes a label of a Dodecahedron as the String parameter and returns the corresponding Dodecahedron object if found in the DodecahedronList2 object; otherwise returns null.  <u>Case should be ignored when attempting to match the</u> <u>label</u>.</li>

 <li>deleteDodecahedron: Takes a String as a parameter that represents the label of the Dodecahedron and returns the Dodecahedron if it is found in the DodecahedronList2 object and deleted; otherwise returns null.  <u>Case should be ignored when attempting to</u> <u>match the label; consider calling/using </u><u>findDodecahedron in this method</u>.  When an element is deleted from an array, elements to the right of the deleted element must be shifted to the left. After shifting the items to the left, the last Dodecahedron element in the array should be set to null.  Finally, the number of elements field must be decremented.</li>

 <li>editDodecahedron: Takes three parameters (label, color, and edge), uses the label to find the corresponding the Dodecahedron object in the list.  If found, sets the color and edge to the values passed in as parameters, and returns true.  If not found, returns false.</li>

</ul>

<strong> </strong>

<strong>Code and Test</strong>: Remember to import java.util.Scanner, java.io.File, java.io.IOException.  These classes will be needed in the readFile method which will require a throws clause for IOException.

Some of the methods above require that you use a loop to go through the objects in the array.  You may want to implement the class below in parallel with this one to facilitate testing.  That is, after implementing one to the methods above, you can implement the corresponding “case” in the switch for menu described below in the DodecahedronList2MenuApp class.




<ul>

 <li><strong>DodecahedronList2MenuApp.java </strong>(replaces DodecahedronListMenuApp class from Project 6; <u>the file and class name in the file must be renamed to reflect DodecahedronList2MenuApp</u>).  <strong>To rename an existing .java file, open the file in jGRASP, change the name of the class in the source code, and then click the Save button.  In the dialog that pops up, click the “Rename and Save” button.  This will rename the .java file and delete the old associated .class file.  <u>Be</u> <u>sure to make these changes in your main method as necessary.</u></strong></li>

</ul>




<strong>Requirements</strong>: Create a DodecahedronList2MenuApp class with a main method that presents the user with a menu with eight options, each of which is implemented to do the following: (1) read the input file and create a DodecahedronList2 object, (2) print the DodecahedronList2 object, (3) print the summary for the DodecahedronList2 object, (4) add a Dodecahedron object to the DodecahedronList2 object, (5) delete a Dodecahedron object from the DodecahedronList2 object, (6) find a Dodecahedron object in the DodecahedronList2 object, (7) Edit a Dodecahedron object in the DodecahedronList2 object, and (8) quit the program.




<strong>Design</strong>:  The main method should print a list of options with the action code and a short description followed by a line with just the action codes prompting the user to select an action.  After the user enters an action code, the action is performed, including output if any.  Then the line with just the action codes prompting the user to select an action is printed again to accept the next code.  The first action a user would normally perform is ‘R’ to read in the file and create a DodecahedronList2 object.  However, the other action codes should work even if an input file has not been processed. The user may continue to perform actions until ‘Q’ is entered to quit (or end) the program.  Note that your program should accept both uppercase and lowercase action codes.       Below is output produced after printing the action codes with short descriptions followed by the prompt with the action codes waiting for the user to make a selection.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345678910</td>

   <td width="511">Dodecahedron List System MenuR – Read File and Create Dodecahedron ListP – Print Dodecahedron ListS – Print SummaryA – Add DodecahedronD – Delete DodecahedronF – Find DodecahedronE – Edit DodecahedronQ – QuitEnter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

Below shows the screen after the user entered ‘r’ and then (when prompted) the file name.  Notice the output from this action was “File read in and Dodecahedron List created”.  This is followed by the prompt with the action codes waiting for the user to make the next selection.  You should use the <em>dodecahedron_data_1.txt </em>file from Project 5 to test your program.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345</td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: rFile name: dodecahedron_data_1.txtFile read in and Dodecahedron List created Enter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘p’ to Print Dodecahedron List is shown below and next page.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345678910111213141516171819 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: pDodecahedron Test List Dodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777 Dodecahedron “Medium Example” is “orange” with 30 edges of length 10.1 units.surface area = 2,106.071 square units    volume = 7,895.319 cubic units    surface/volume ratio = 0.267 Dodecahedron “Large Example” is “silver” with 30 edges of length 200.5 units.surface area = 829,963.459 square units    volume = 61,765,889.248 cubic units    surface/volume ratio = 0.013 Enter Code [R, P, S, A, D, F, E, or Q]:<em> </em></td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘s’ to print the summary for the list is shown below.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567891011 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: s —– Summary for Dodecahedron Test List —–Number of Dodecahedrons: 3Total Surface Area: 832,070.821Total Volume: 61,773,784.687Average Surface Area: 277,356.94Average Volume: 20,591,261.562Average Surface/Volume Ratio: 3.686Enter Code [R, P, S, A, D, F, E, or Q]:<em> </em></td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘a’ to add a Dodecahedron object is shown below.  Note that after

‘a’ was entered, the user was prompted for label, color, and edge.  Then after the Dodecahedron object is added to the Dodecahedron List, the message “*** Dodecahedron added ***” was printed.  This is followed by the prompt for the next action. After you do an “add”, you should do a “print” or a “find” to confirm that the “add” was successful.







<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567</td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: aLabel: d1Color: goldEdge: 5.8*** Dodecahedron added ***Enter Code [R, P, S, A, D, F, E, or Q]:<em> </em></td>

  </tr>

 </tbody>

</table>




Here is an example of the successful “delete” for a Dodecahedron object, followed by an attempt that was not successful (i.e., the Dodecahedron object was not found).  Do “p” to confirm the “d”.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">123456789</td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: dLabel: Medium Example“Medium Example” deleted Enter Code [R, P, S, A, D, F, E, or Q]: dLabel: not a real object“not a real object” not found Enter Code [R, P, S, A, D, F, E, or Q]: </td>

  </tr>

 </tbody>

</table>




Here is an example of the successful “find” for a Dodecahedron object, followed by an attempt that was <u>not</u> successful (i.e., the Dodecahedron object was not found).




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">123456789101112 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: fLabel: small EXAMPLEDodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.    surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777 Enter Code [R, P, S, A, D, F, E, or Q]: fLabel: tiny obj“tiny obj” not found Enter Code [R, P, S, A, D, F, E, or Q]: </td>

  </tr>

 </tbody>

</table>

<strong> </strong>




Next is an example of the successful “edit” for a Dodecahedron object, followed by an attempt that was <u>not</u> successful (i.e., the Dodecahedron object was not found).  In order to verify the edit, you should do a “find” for “wide example” or you could do a “print” to print the whole list.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345678910111213</td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: eLabel: small EXAMPLEColor: greenEdge: 0.1“small EXAMPLE” successfully editedEnter Code [R, P, S, A, D, F, E, or Q]: eLabel: not thereColor: yellowEdge: 12.4“not there” not foundEnter Code [R, P, S, A, D, F, E, or Q]:<em> </em></td>

  </tr>

 </tbody>

</table>




Finally, below is an example of entering an invalid code, followed by an example of entering a ‘q’ to quit the application with no message.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345</td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: b*** invalid code *** Enter Code [R, P, S, A, D, F, E, or Q]: q—-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong>Code and Test</strong>:

<u>Important considerations</u>:  This class should import java.util.Scanner and java.io.IOException.  Carefully consider the following information as you develop this class.




<ol>

 <li>At the beginning of your main method, you should declare and create an array of</li>

</ol>

Dodecahedron objects and then declare and create a DodecahedronList2 object using the list name, the array, and 0 as the parameters in the constructor.  This will be a DodecahedronList2 object that contains no Dodecahedron objects.  For example:

String _______ = <strong>“</strong>*** no list name assigned ***”;  Dodecahedron[] _________ = new Dodecahedron[100];

DodecahedronList2 _________ = new DodecahedronList2(_________,_________,_________);




The ‘R’ option in the menu should invoke the readFile method on your DodecahedronList2 object.  This will return a new DodecahedronList2 object based on the data read from the file, and this new DodecahedronList2 object should replace (be assigned to) your original DodecahedronList2 object variable in main.  Since the readFile method throws IOException, your main method needs to do this as well.




<ol start="2">

 <li><strong><u>Very Important</u></strong>: <strong><u>You should declare only one Scanner on System.in for your entire</u> <u>program, and this should be done in the main method</u>. </strong>That is, all input from the keyboard (System.in) must be done in your <em>main</em> method. Declaring more than one Scanner on System.in in your program will likely result in a very low score from Web-CAT.</li>

</ol>







<h1>         Page</h1>

<ol start="3">

 <li>For the menu, your switch statement expression should evaluate to a char and each case should be a char; alternatively, your switch statement expression should evaluate to a String with a length of 1 and each case should be a String with a length of 1.</li>

</ol>




After printing the menu of actions with descriptions, you should have a <em>do-while</em> loop that prints the prompt with just the action codes followed by a switch statement that performs the indicated action.  The <em>do-while</em> loop ends when the user enters ‘q’ to quit.  You should strongly consider using a <em>for-each</em> loop as appropriate in the new methods that require you to search the list.  You should be able to test your program by exercising each of the action codes.  After you implement the “Print Dodecahedron List” option, you should be able to print the DodecahedronList2 object after operations such as ‘A’ and ‘D’ to see if they worked.  You may also want to run in debug mode with a breakpoint set at the switch statement so that you can step-into your methods if something is not working.  In conjunction with running the debugger, you should also create a canvas drag the items of interest (e.g., the Scanner on the file, your DodecahedronList2 object, etc.) onto the canvas and save it.  As you play or step through your program, you’ll be able to see the state of these objects change when the ‘R’, ‘A’, and ‘D’ options are selected.




Although your program may not use all of the methods in your Dodecahedron and

DodecahedronList2 classes, you should ensure that all of your methods work according to the specification.  You can run your program in the canvas and then after the file has been read in, you can call methods on the DodecahedronList2 object in interactions or you can write another class and main method to exercise the methods.  Web-CAT will test all methods to determine your project grade.

<h1></h1>