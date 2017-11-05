<h1>Description</h1>
    
This plugin asks your Jenkins-server continously for the states of the jobs. The worst state will be shown as an icon in the IntelliJ-IDEA-Toolbar and
    a notification will inform you about this state. Additionally it will play a sound, if you like.

You can click on the icon to see the full list of jobs and a double-click on an item of this list will open your browser.

<h1>Usage</h1>
<h2>Prepare your Jenkins</h2>

You must have installed the REST-API-Plugin inside your Jenkins-server. When it was active, you will see a link to the REST-API on the
bottom-right of any page.

When you choose a view or a dashboard on Jenkins, click on this link and then click on the link "XML-API", you will get the url of the XML-REST-API of this dashboard.
This is necessary for the next steps.

<h2>Configuration</h2>
<p>In the settings go to "Tools/Jenkins State".<br>
<ul>
    <li>Enable the plugin for the current project.</li>
    <li>Insert the XML-REST-API-url into the textfield. There is also a small Helper for creating this url.</li>
    <li>If your Jenkins requires authentication, you must enter your username and your API-Token (NOT your password!) in the following fields. You will find your token in your user-settings in Jenkins.</li>
    <li>The plugin will check every 10 seconds for a new state. You can change this frequency in the settings.</li>
    <li>Jenkins will show a passed state with a blue icon. You can change this to green, for a normal traffic light.</li>
    <li>Select the type of colors, which should show a notification and would play a sound. Normally only when a problem comes up, there should be a notification, so the default is ok.</li>
</ul>
</p>

<h1>Additional feature</h1>
<p>In our company, nobody is allowed to checkin to our VCS, when the state of any job is red, but only for fixes of this error to make the state blue.
This is because any other checkin may confuse debugging the error.<br>
The plugin adds a checkbox in the checkin-dialog. When this is selected, IDEA warns you, when the state is worse during a checkin.</p>

<h1>Remarks</h1>
    Icons from <a href="http://www.fatcow.com/free-icons">http://www.fatcow.com/free-icons</a>
