## [Ithaca College status page](https://itstatus.ithaca.edu/): 


### Project description
The current status page for Ithaca colleges IT infrastructure. Seperate from the core infrastructure this page acts as a place for students to go to guage whether or not an issue that they are having is related to their own personal computer/network or if it is a college wide outage. This page also notifies the relevant parties about a client facing outage as soon as it occurs. I have also configured it to send notification to an internal teams channel that is watched by all stake holder for the different aspects of the status page.   
 

### Project technologies 
---
<table>
  <tr>
     <td>Hund</td>
     <td>Description</td>
 </tr>
  <tr>
    <td><img src="images/hundlogo.jpg"  width="100"  height="100" style="border-radius:50%"/></td>
    <td>The status page SAAS platform hund for it's cost effective pricing model and good utility to build status page components that are linked to the relevant wedsites and servers on which the web services are run. Upon an outage hund sends out notifications to subscribers to notify them of changes within the infrastructure.</td>
  </tr> 
  <tr>
     <td>Datadog</td>
     <td>Description</td>
 </tr> 
  <tr>
    <td><img src="images/Datadog_Logo.jpg"  width="100"  height="100" style="border-radius:50%"/></td>
    <td>The monitoring SAAS Datadog is what the college uses to monitor each of the different systems that are run on the infrastructure. As the Admin for it I have leveraged a series of webhooks to broadcast the system status of key servers that I can then relay to Hund to get the most up to date information of key services. Doing this allows the servers themselves to be isolated from the internet behind a firewall but still have an external service that isn't dependant on the colleges infrastructure to report the current status of the systems in question. I have also configured a wide variety of services within datadog to help with visibility and monitoring for the varius stakeholders. </td>
  </tr> 
 <tr>
     <td>Azure </td>
     <td>Description</td>
 </tr> 
 <tr>
    <td><img src="images/azurelogo.jpg"  width="100"  height="100" style="border-radius:50%"/></td>
    <td>Utilized Azure platform SAAS Logic-apps to take information broadcast by datadog for the servers, websites and services that are utilized by the colloege and translated them into the expected formats that Hund's webhook listensers could accept. This allowed me to connect our infrasturture to our status page, automating the notification process.</td>
  </tr> 
  <tr>
     <td>JavaScript</td>
     <td>Description</td>
  </tr> 
  <tr>
    <td><img src="images/teams-logo.png"  width="100"  height="100" style="border-radius:50%"/></td>
    <td>Leveraged the microsoft connector cards within in teams to style the messages that were posted there by my azure logic-app service. This way the message that was posted gave an easy to read message along with a clickable button within teams that would lead the user back to the status page, and more specifically to the component  that was the one having the issue. I dynamically filled out the connector card api with information sent out by the status page upon a change in status routed through azure logic-apps to properly format the information so that teams could display it the way I wanted it to. </td>
  </tr> 
</table>

---

#### Project status:   [In Production] 
#### Project type:     [Work project]  
#### View status:      [Private] 

--- 


---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
