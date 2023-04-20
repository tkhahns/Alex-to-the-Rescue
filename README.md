<h1>Power consumption app </h1>

<h2>Table of contents</h2>
<ul>
  <li>Criteria to measure power consumption</li>
  <li>How to run the test program</li>
  <li>Making of program using python</li>
  <li>Inclusion of HTML and flask to render web application</li>
  <li>Future scope</li>
</ul>
<hr/>

<h2>Criteria to measure power consumption</h2>
<p>From online research, 6 main metrics were found to measure power consumption: CPU usage, GPU usage, Disk usage, Network usage, RAM usage, and screen brightness. Out of these CPU and GPU usage were not ideal as the metric depended on measuring battery consumption which is affected by large number of factors and disk usage is also not the most accurate metric. Therefore, for a small scale program, Network and RAM usage were chosen as the key criteria to measure power consumption.

However, the program can be easily implemented for additional measurement metrics using the same function structure that was used for RAM and Network usage (See <b>Future Scope</b> section for more information).</p>

<h2>How to run the test program</h2>
<ol>
  <li>Make sure psutil and flask are installed on your device (pip install psutil/pip install flask)</li>
  <li>Download the power consumption app zip file and unzip</li>
  <li>On terminal, go to the power consumption app directory and run the app.py file using the command: python app.py</li>
  <li>The url of the website should be http://127.0.0.1:5000 . This can be double checked by seeing the display on terminal (*Running on:)</li>
  <li>If it is running on an alternate URL enter that URL, otherwise enter http://127.0.0.1:5000 into a new browser window</li>
  <li> Follow the steps mentioned on the website and click the button. Then wait for a while to see the output</li>
  <li>In terminal, click ctrl+C to terminate the program and close the tab on the web browser.
</ol>

<h2>Making of program using python </h2>
<ol>
<li> The app uses the <b>Psutil</b> library to get the information for the RAM and network usage metrics. For RAM usage, the Process ID (pid) is also required.</li>
<li>A function is created for each metric which when called gives the power consumed by the application for that metric</li>
 </ol>
<p>(Further information about specific processes can be found in documentation of the program files.)</p>

<h2>Inclusion of HTML and flask to render web application</h2>
<ol>
<li>Basic HTML was used to develop a simple web page with a text-box to enter the application name and a button</li>
<li>The button, when clicked, submits the app name to the flask program</li>
<li>The flask program then computes the relevant power consumption and displays the values by updating an output div present in the HTML file</li>
<li>As a result, the user is shown the power consumption by RAM and network usage, and the total power consumption</li>
</ol>
<p>(Further information about specific processes can be found in documentation of the program files.)</p>

<h2>Future Scope</h2>
<p>Since the psutil library can be used to get the process ID of any application, additional metrics can be used to give a more accurate power consumption value using the following steps:</p>
<ol>
  <li>Find the relevant psutil process to measure the metric</li>
  <li>Use the same function template as RAM and Network usage to return the power consumption of the metric (Some additional information such as conversion values will be required)</li>
  <li> Call the function for the new metric in the flask program and assign it to a variable</li>
  <li> Add this variable to the list of variables rendered in the "output" div in the index.html file</li>

