# Huginn Wohnungssuche

This is a collection of [Huginn](http://www.opensourcerails.com/huginn/) Agents for apartment searches in Germany. It will check the sites in a defined interval and notifies you immediately about new apartments.

They agents come bundled in a scenario which you can import into your Huginn instance. After that you can change the Site URLs to match your search parameters, or add new pages you like to watch.

You can configure multiple notification channels, for example [Pushover](https://pushover.net/) or a Slack channel (see the Huginn documentation!).  

## Add new sites / how it works

1. You need to know if the URL parameters for your search settings are visible in the URL, so you can use it with the Huginn WebsiteAgent.
2. You need to know if the site relies on JavaScript, and if so, you need to configure the PhantomJSCloudAgent first, to get Static HTML for the WebsiteAgent to check
3. Check if you can isolate the listing item title/link with CSS/XPath queries, if so you can use the FormatWithDetail formatter, and get notifications about each new item. If not you can only use FormatWihtNoDetail and you just get a notification that there is something new on the page
4. Configure your preferred notification method, Pushover and Slack are included as examples.


Created by [@MoStueck](https://twitter.com/MoStueck/) and [@stroebjo](https://twitter.com/stroebjo).


