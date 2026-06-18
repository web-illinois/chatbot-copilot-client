# chatbot-copilot-client
Contains template code that can be added to a website to integrate with Copilot Studio. University branded and vetted for accessibility.

This was generated as part of the IT ProForum 2026 presentation. Links are at:

* https://itproforum.illinois.edu/eventdesc/1-spring-2026/1-1pm/from-idea-to-agent-building-your-first-chatbot-with-copilot-studio/
* https://go.illinois.edu/itpf2026-resources

## Files in /src directory

* chatbot.js: JavaScript that contains chatbot connection information
* chatbot.css: CSS style that contains chatbot styling

## How to set up

Your HTML file needs needs to have the following in the head tag:
```
    <script src="https://cdn.botframework.com/botframework-webchat/latest/webchat.js"></script>
    <script src="//cdn.toolkit.illinois.edu/illinois-webchat/latest/chatbot.js"></script>
    <link rel="stylesheet" href="//cdn.toolkit.illinois.edu/illinois-webchat/latest/chatbot.css"></script>
```

Then in the body where you want the button, add this:
```
<div id="illinois-webchat" role="none"
     data-endpoint="[insert endpoint]"
     data-bot-image=""
     data-user-image=""></div>
```

You get the endpoint by going to Copilot Studio Agent and choosing Channels --> Email. Copy the token endpoint for this. 

![Screenshot of the email section of the Copilot Studio](image.png)

Put this endpoint in the `data-endpoint` attribute in the `<div>` tag. 

For `data-bot-image` and `data-user-image` attributes, you can include paths to images. If you delete these attributes, it will default to generic images.

Example (note that we have a custom bot image but a default user image):
```
<div id="illinois-webchat" role="none"
     data-endpoint="https://default000000000000000000000000000000000.e3.environment.api.powerplatform.com/powervirtualagents/botsbyschema/cr29b_xxxxxx/directline/token?api-version=2022-03-01-preview"
     data-bot-image="/img/bot.png"></div>
```

### Resources

* https://learn.microsoft.com/en-us/azure/bot-service/bot-builder-webchat-overview?view=azure-bot-service-4.0 
* https://uofi.app.box.com/s/qa548vopkunb0aolpri0yb8uml5wu5d1 -- the campus Agent Blueprint Worksheet

## Activation

You can start the chatbot by calling `showChat()` on a button click. Note that when this starts, it will use a Copilot Credit, so only do this when the user wants to intiate a chat. Do not run this on `window.load()`.

### Copilot Licensing Links:

* https://azure.microsoft.com/en-us/pricing/details/copilot-studio/
* https://learn.microsoft.com/en-us/microsoft-365/copilot/pay-as-you-go/copilot-capacity-packs 



