---


---

<h2 id="subscription-center-logic">Subscription Center Logic:</h2>
<p>When sending emails / journeys, the following data extensions are updated when a customer decides to subscribe or unsubscribe:</p>
<h3 id="for-residents-filtered-from-residents_all">For Residents (filtered from Residents_All):</h3>
<ol>
<li>Residents_All_Services_and_Promotions</li>
<li>Residents_All_Property_Events</li>
</ol>
<h3 id="for-service-providers-filtered-from-service_providers_all">For Service Providers (Filtered from Service_Providers_All):</h3>
<ol>
<li>Service_Providers_Amenify_Updates</li>
<li>Service_Providers_Monthly_Newsletter</li>
</ol>
<h3 id="for-property-managers-filtered-from-property_managers_all">For Property Managers (Filtered from Property_Managers_All):</h3>
<ol>
<li>Property_Managers_Amenify_Updates</li>
<li>Property_Managers_Monthly_Newsletter</li>
</ol>
<p>These data extensions are filtered data extensions.  When sending an email you should never send from the data extensions from which these are filtered.  Eg. do not send from Residents_All.   Instead send from the Data Extensions listed above.</p>
<p>The following Publication Lists are also updated so that subscription data can effectively be tracked.  Marketing cloud data is calculated based off of the publication lists.  Because of this, it is very important to associate your emails with a publication list when you are choosing the target from your Data Extension.</p>
<ol>
<li>Service Providers</li>
<li>Property Managers</li>
<li>Residents</li>
</ol>
<h3 id="sending-emails">Sending Emails</h3>
<ol>
<li>When sending emails and choosing a target, remember to choose the Data Extension for the relevant content you wish to send emails.  Eg. if you want to send to a Resident and It’s regarding Services and promotions, then choose the Residents_All_Services_and_Promotions data extension as your target.</li>
<li>Associate the proper Publication list with the Target as well.  Eg. when sending emails to Residents_All_Services_and_Promotions, be sure to associate the “Residents” Publication list with your email.</li>
</ol>
<p>The filtered data extensions are the “source of truth” in terms of accurate subscription data.   The filtered data extensions are the DE’s mentioned at the top of this documentation.</p>

