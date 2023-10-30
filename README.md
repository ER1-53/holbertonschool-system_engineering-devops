<h1>Web infrastructure design</h1>

<h2>Resources</h2>

<p><strong>Read or watch</strong>:</p>

<ul>
<li><strong>Network basics</strong> concept page</li>
<li><strong>Server</strong> concept page</li>
<li><strong>Web server</strong> concept page</li>
<li><strong>DNS</strong> concept page</li>
<li><strong>Load balancer</strong> concept page</li>
<li><strong>Monitoring</strong> concept page</li>
<li><a href="/rltoken/7Pp0_Mdit6r_ZdRGKAwcqw" title="What is a database" target="_blank">What is a database</a> </li>
<li><a href="/rltoken/YqKvabbDDtSjnHMV9g1gHw" title="What&#39;s the difference between a web server and an app server?" target="_blank">What&rsquo;s the difference between a web server and an app server?</a></li>
<li><a href="/rltoken/kZXE57FUOK-cqmLfN3CWfg" title="DNS record types" target="_blank">DNS record types</a> </li>
<li><a href="/rltoken/56OIJ23o5mqSaSeLEwxzJg" title="Single point of failure" target="_blank">Single point of failure</a> </li>
<li><a href="/rltoken/lxwkY5pRIVzatMPXwx6yew" title="How to avoid downtime when deploying new code" target="_blank">How to avoid downtime when deploying new code</a> </li>
<li><a href="/rltoken/rITwKN4AKP1hXZl2FKcAcw" title="High availability cluster (active-active/active-passive)" target="_blank">High availability cluster (active-active/active-passive)</a> </li>
<li><a href="/rltoken/iEaO7X54UemiSN9z8TtFVA" title="What is HTTPS" target="_blank">What is HTTPS</a> </li>
<li><a href="/rltoken/P2A36USOkcekiqHsCzTefQ" title="What is a firewall" target="_blank">What is a firewall</a> </li>
</ul>

<h2>Learning Objectives</h2>

<p>At the end of this project, you are expected to be able to <a href="/rltoken/RrkQ3Y4e2NeMFLApRBf8Zg" title="explain to anyone" target="_blank">explain to anyone</a>, <strong>without the help of Google</strong>:</p>

<h3>General</h3>

<ul>
<li>You must be able to draw a diagram covering the web stack you built with the sysadmin/devops track projects</li>
<li>You must be able to explain what each component is doing</li>
<li>You must be able to explain system redundancy</li>
<li>Know all the mentioned acronyms: LAMP, SPOF, QPS</li>
</ul>

<h2>Requirements</h2>

<h3>General</h3>

<ul>
<li>A <code>README.md</code> file, at the root of the folder of the project, is mandatory</li>
<li>For each task, once you are done whiteboarding (on a whiteboard, piece of paper or software or your choice), take a picture/screenshot of your diagram</li>
<li>This project will be manually reviewed:</li>
<li>As each task is completed, the name of that task will turn green</li>
<li>Upload a screenshot, showing that you completed the required levels, to any image hosting service (I personally use <a href="/rltoken/16_BGzDlaeQepe6t265Xag" title="imgur" target="_blank">imgur</a> but feel free to use anything you want). </li>
<li>For the following tasks, insert the link from of your screenshot into the answer file </li>
<li>After pushing your answer file to GitHub, insert the GitHub file link into the URL box</li>
<li>You will also have to whiteboard each task in front of a mentor, staff or student - no computer or notes will be allowed during the whiteboarding session</li>
<li>Focus on what you are being asked: </li>
<li>Cover what the requirements mention, we will explore details in a later project</li>
<li>Keep in mind that you will have 30 minutes to perform the exercise, you will get points for what is asked in requirements</li>
<li>Similarly in a job interview, you should answer what the interviewer asked for, be careful about being too verbose - always ask the interviewer if going into details is necessary - speaking too much can play against you</li>
<li>In this project, again, avoid going in details if not asked</li>
</ul>


<details>
<summary>Click to see: Tasks</summary>

<h3 class="panel-title">
0. Simple web stack
</h3>

A lot of websites are powered by simple web infrastructure, a lot of time it is composed of a single server with a <a href="/rltoken/OtZFy7tXzJmziqfiXKT5lA" title="LAMP stack" target="_blank">LAMP stack</a>.</p>

<p>On a whiteboard, design a one server web infrastructure that hosts the website that is reachable via <code>www.foobar.com</code>. Start your explanation by having a user wanting to access your website.</p>

<p>Requirements:</p>

<ul>
<li> You must use:

<ul>
<li>1 server</li>
<li>1 web server (Nginx)</li>
<li>1 application server</li>
<li>1 application files (your code base)</li>
<li>1 database (MySQL)</li>
<li>1 domain name <code>foobar.com</code> configured with a <code>www</code> record that points to your server IP <code>8.8.8.8</code></li>
</ul></li>
<li>You must be able to explain some specifics about this infrastructure:

<ul>
<li>What is a server</li>
<li>What is the role of the domain name</li>
<li>What type of DNS record <code>www</code> is in <code>www.foobar.com</code></li>
<li>What is the role of the web server</li>
<li>What is the role of the application server</li>
<li>What is the role of the database</li>
<li>What is the server using to communicate with the computer of the user requesting the website</li>
</ul></li>
<li>You must be able to explain what the issues are with this infrastructure:

<ul>
<li>SPOF</li>
<li>Downtime when maintenance needed (like deploying new code web server needs to be restarted)</li>
<li>Cannot scale if too much incoming traffic</li>
</ul></li>
</ul>

<p>Please, remember that everything must be written in English to further your technical ability in a variety of settings.</p>

</div>

<div class="list-group">
<!-- Task URLs -->

<!-- Technical information -->
<div class="list-group-item">
<p><strong>Repo:</strong></p>
<ul>
<li>GitHub repository: <code>holbertonschool-system_engineering-devops</code></li>
<li>Directory: <code>web_infrastructure_design</code></li>
<li>File: <code>0-simple_web_stack</code></li>
</ul>
</div>

<h3 class="panel-title">
1. Distributed web infrastructure
</h3>

On a whiteboard, design a three server web infrastructure that hosts the website <code>www.foobar.com</code>.</p>

<p>Requirements:</p>

<ul>
<li> You must add:

<ul>
<li>2 servers</li>
<li>1 web server (Nginx)</li>
<li>1 application server</li>
<li>1 load-balancer (HAproxy)</li>
<li>1 set of application files (your code base)</li>
<li>1 database (MySQL)</li>
</ul></li>
<li>You must be able to explain some specifics about this infrastructure:

<ul>
<li>For every additional element, why you are adding it</li>
<li>What distribution algorithm your load balancer is configured with and how it works</li>
<li>Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both</li>
<li>How a database Primary-Replica (Master-Slave) cluster works</li>
<li>What is the difference between the Primary node and the Replica node in regard to the application</li>
</ul></li>
<li>You must be able to explain what the issues are with this infrastructure:

<ul>
<li>Where are SPOF</li>
<li>Security issues (no firewall, no HTTPS)</li>
<li>No monitoring</li>
</ul></li>
</ul>

<p>Please, remember that everything must be written in English to further your technical ability in a variety of settings.</p>

</div>

<div class="list-group">
<!-- Task URLs -->

<!-- Technical information -->
<div class="list-group-item">
<p><strong>Repo:</strong></p>
<ul>
<li>GitHub repository: <code>holbertonschool-system_engineering-devops</code></li>
<li>Directory: <code>web_infrastructure_design</code></li>
<li>File: <code>1-distributed_web_infrastructure</code></li>
</ul>
</div>

<h3 class="panel-title">
2. Secured and monitored web infrastructure
</h3>

On a whiteboard, design a three server web infrastructure that hosts the website <code>www.foobar.com</code>, it must be secured, serve encrypted traffic, and be monitored.</p>

<p>Requirements:</p>

<ul>
<li> You must add:

<ul>
<li>3 firewalls </li>
<li>1 SSL certificate to serve <code>www.foobar.com</code> over HTTPS</li>
<li>3 monitoring clients (data collector for Sumologic or other monitoring services)</li>
</ul></li>
<li>You must be able to explain some specifics about this infrastructure:

<ul>
<li>For every additional element, why you are adding it</li>
<li>What are firewalls for</li>
<li>Why is the traffic served over HTTPS</li>
<li>What monitoring is used for</li>
<li>How the monitoring tool is collecting data</li>
<li>Explain what to do if you want to monitor your web server QPS</li>
</ul></li>
<li>You must be able to explain what the issues are with this infrastructure:

<ul>
<li>Why terminating SSL at the load balancer level is an issue</li>
<li>Why having only one MySQL server capable of accepting writes is an issue</li>
<li>Why having servers with all the same components (database, web server and application server) might be a problem</li>
</ul></li>
</ul>

<p>Please, remember that everything must be written in English to further your technical ability in a variety of settings.</p>

</div>

<div class="list-group">
<!-- Task URLs -->

<!-- Technical information -->
<div class="list-group-item">
<p><strong>Repo:</strong></p>
<ul>
<li>GitHub repository: <code>holbertonschool-system_engineering-devops</code></li>
<li>Directory: <code>web_infrastructure_design</code></li>
<li>File: <code>2-secured_and_monitored_web_infrastructure</code></li>
</ul>
</div>

<h3 class="panel-title">
3. Scale up
</h3>

Readme</p>

<ul>
<li><a href="/rltoken/QHWrcB0kVYwbgWCsL57mkQ" title="Application server vs web server" target="_blank">Application server vs web server</a></li>
</ul>

<p>Requirements:</p>

<ul>
<li> You must add:

<ul>
<li>1 server</li>
<li>1 load-balancer (HAproxy) configured as cluster with the other one</li>
<li>Split components (web server, application server, database) with their own server</li>
</ul></li>
<li>You must be able to explain some specifics about this infrastructure:

<ul>
<li>For every additional element, why you are adding it</li>
</ul></li>
</ul>

<p>Please, remember that everything must be written in English to further your technical ability in a variety of settings.</p>

</div>

<div class="list-group">
<!-- Task URLs -->

<!-- Technical information -->
<div class="list-group-item">
<p><strong>Repo:</strong></p>
<ul>
<li>GitHub repository: <code>holbertonschool-system_engineering-devops</code></li>
<li>Directory: <code>web_infrastructure_design</code></li>
<li>File: <code>3-scale_up</code></li>
</ul>
</div>

</details>
