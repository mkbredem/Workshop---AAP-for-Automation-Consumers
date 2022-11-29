<!-- Output copied to clipboard! -->

<!-----

You have some errors, warnings, or alerts. If you are using reckless mode, turn it off to see inline alerts.
* ERRORs: 0
* WARNINGs: 0
* ALERTS: 10

Conversion time: 2.434 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Tue Nov 29 2022 03:11:29 GMT-0800 (PST)
* Source doc: Darden - Automation Consumer Lab - Markdown
* Tables are currently converted to HTML tables.
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!

----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 10.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>
<a href="#gdcalert7">alert7</a>
<a href="#gdcalert8">alert8</a>
<a href="#gdcalert9">alert9</a>
<a href="#gdcalert10">alert10</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



# Darden - Automation Consumer Lab


## Summary of Exercises

Each student will have their own Ansible Automation Platform Controller environment that is able to manage 2 nodes.  A Red Hat Enterprise Linux server (node1) and a Windows 2016 server (win1).  For the purposes of this exercise, we will only be focusing on managing/automating the win1 node.  The primary goal is to get students familiar with how to navigate within Automation Controller in order to execute jobs/playbooks and review output.


## Exercise 1 - Accessing Your Environment


### 
    Go to: [https://play.instruqt.com/embed/redhat/tracks/product-demos-dev](https://play.instruqt.com/embed/redhat/tracks/product-demos-dev)


### Launch Lab



* Click the green “Launch” button (wait approx 6 minutes)
* Click the green “Start” button


### Log in to Automation Controller


<table>
  <tr>
   <td>USERNAME
   </td>
   <td><strong>admin</strong>
   </td>
  </tr>
  <tr>
   <td>PASSWORD
   </td>
   <td><strong>ansible123!</strong>
   </td>
  </tr>
</table>



## 


## Exercise 2 - Explore Automation Controller Resources

Automation Controller **resources** consist of Credentials, Projects, Inventories, and Templates.  You can jump to available resources in the left hand navigation.

Tip: Left hand navigation may be hidden.  Click on the 3 bars in the top menu to expand it (see Red Box in image to the left).  Read descriptions below as you Click on each of the resources to explore and see what options they provide.

As an Automation Consumer, you will not need to modify any of these, it is just to provide you with the anatomy of automation.



* Projects → Review: <span style="text-decoration:underline;">Ansible Official Demo Project</span> 

                        Defines a source code repository such as github, gitlab, or Azure Devops (to name a few).  This is where the playbooks that have been written live and are version controlled. 

* Credentials → Review: <span style="text-decoration:underline;">Controller Credential</span>

                        Represent all the secrets needed throughout the automation process.  Examples include credentials to access: 

    * your playbook in the git repository
    * the node/server you are automating
    * cloud providers’ api’s for provisioning 
    * And much more… \

* Inventories → Review: <span style="text-decoration:underline;">Workshop Inventory</span>

                        A manifest of nodes within your environment that you intend to automate.  Inventories will contain hosts and/or groups of hosts, so you can target either one node, a group of similar/related nodes, or the entire inventory.

* Templates → Review: <span style="text-decoration:underline;">SETUP</span>

    Templates are used to run Ansible Playbooks that have been written by content creators and domain experts.  However, these templates need a lot of information in order to launch the playbooks.  That is where the other resources we just reviewed come in.  In order to launch a Template, you will need to add the other resources to the job template definition.  The fields collected in the job template should look very familiar (projects, credentials, inventories, and more).


    Note: Don't exit out of the SETUP Job Template, as we will be using it for exercise 3 below.



## 


## Exercise 3 - Launch a Job Template

As an End User, or Consumer of Ansible, this is where you will be spending all of your time.  You will not need to view or edit any of the other resources other than Templates.  All Job templates (single playbook) and Workflow Job Templates (series of playbooks) are launched with the simple click of a button.


### Click the Launch button in the SETUP job template:


    

<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")



### 
    


### 
    Select **Windows** for the Demo Category


    Playbooks can use variables supplied via a form (called a Survey) that can dynamically define how the playbook is run.  In this particular case, we are executing a Job Template that automates the build of many more job templates for you to play around with.  Depending on which Category you select, will dictate which job templates are added to the Automation Controller.  


    Go ahead and select **windows** in the drop down listbox, then click the **Next** button

<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")



    On the subsequent preview screen you are given the opportunity to review the Job Template configuration.  Once settings are confirmed, click the **Launch** button


### Review the Job Template output


    On the subsequent screen you will see the output of the playbook.  This is critical from an auditing perspective.  Automaton Controller centrally logs all the jobs that have been executed with key information such as who launched it, when it was launched, the duration, and the exact changes that were made on each of the systems that were targeted. 


    Scroll through the output to see the user-friendly task definitions that explain what the task is doing (highlighted by the red boxes).


    

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")



### 
    See the Fruits of our button clicks:



* Go back to Templates (under **Resources** in the left hand navigation)
* See all the recently added Job Templates with the **WINDOWS /…** prefix that were built to help you automate your windows environment.


## Exercise 4 - Automate Windows with Job Templates

Now that we can play around with these new job templates and see how easy it is to perform some otherwise complex and time consuming tasks.  To top it all off, because you are only having to click buttons and answer simple questions there is very little margin for human error..



* **Install Software**

    Got to **Templates**


    Click the 

<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")
icon next to **WINDOWS** **/ Chocolatey Install Multiple \
**


    Type **win1** in the survey → Click **Next → **Click **Launch**


    Review the output (you just installed nodejs and python on Win1): \


<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")



    Note: You also gathered information about the versions that were installed.

* **Deploy a Website**

    Got to **Templates**


    Click the 

<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")
icon next to **WINDOWS** **/ Install IIS \
**


    Type **win1** for Server Name **&** &lt;whatever you like> for web content  → Click **Next → **Click **Launch**


    Review the output (you just installed IIS, started the service and deployed a website on wiin1):


    

<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image7.png "image_tooltip")



     \
Check out your new custom website that you built (click on the **win1_web** tab at the top of the screen):


    

<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image8.png "image_tooltip")



    You may need to click the **refresh icon** on the top right of the screen:


    

<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image9.png "image_tooltip")


* **Patch a windows server**

    Go to **Templates \
**Click the 

<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image10.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image10.png "image_tooltip")
icon next to **WINDOWS** **/ Patching**


    ** \
**
