### [Link to the Multi-cloud Newsletter Lab sessions](https://b2csa.hubs.vidyard.com/watch/NqzBXdjcQFGPnSyutVP6ai)

# Chat bot Setup
- [Chat bot Setup](#chat-bot-setup)
  - [Omni-Channel Settings:](#omni-channel-settings)
  - [Routing Configurations](#routing-configurations)
  - [Queues:](#queues)
  - [Presence Configurations](#presence-configurations)
  - [Chat Buttons & Invitations](#chat-buttons--invitations)
  - [Deployment:](#deployment)
  - [Embedded Service Deployment](#embedded-service-deployment)
  - [Create a New EINSTEIN Bot](#create-a-new-einstein-bot)
  - [Chat Bot Message Setup](#chat-bot-message-setup)
    - [Add Pre-built Dialogs To The Main Menu](#add-pre-built-dialogs-to-the-main-menu)
    - [Add a New Dialog to the Main Menu](#add-a-new-dialog-to-the-main-menu)
    - [How to Add chatbot to any websites](#how-to-add-chatbot-to-any-websites)

## Omni-Channel Settings:
1. In quick find box, enter “Omni-Channel settings” .
2. Click on “Enable Omni channel”.


## Routing Configurations
1. In quick find box, enter “Routing Configurations”. 
2. Click on New and then fill the required details 
   1. Routing configuration name 
   2. Developer Name
   3. Routing Priority
   4. Select the Routing Model as a Most Available
   5. Unit of capacity.
3. Click on save to create.

## Queues:
1. In quick find box, enter “Queues”. 
2. Click on New and fill in the required details like Label and Queue Name.
3. Select the routing configuration that was created earlier by clicking the search button.
4. Select the supported objects which are Chat Session and Chat transcript.
5. Select the queue members and click on save.


## Presence Configurations
1. In the quick find box, enter “Presence Configurations” .
2. Click on New to create and fill in the required details.
3. Select the Available users and click on save.
4. Presence Statuses
   1. In quick find box, enter “Presence Statuses”
   2. Click on New to create. Fill in the required details.
   3. Select the available Channels. 
   4. Click on Save


## Chat Buttons & Invitations
1. In quick find box, enter “Chat Buttons & Invitations” .
2. Click on New to create and fill the required details.
3. Select the Routing type as “Omni-Channel”.
4. Click on Save.


## Deployment: 
1. In the quick find box, enter “Deployments”.
2. Click on New and fill in the required details.
3. Click on Save.


## Embedded Service Deployment
1. In the quick find box, enter “Embedded Service Deployments”.
2. Click on New Deployment
3. Select the embedded chat.
4. Click on Next.
5. Fill in the required details and click on Save
6. Then click on the chat settings edit button to connect the chat button.
7. Click on the Chat settings edit button.
8. Select the values from dropdowns and click on save.

## Create a New EINSTEIN Bot

1. From Setup, enter Einstein Bots in the Quick Find box, then select Einstein Bots.
2. Click New.
3. The first screen asks you to select the type of bot to build. Select Start from Scratch and click Next.
4. A setup wizard walks you through a few screens to gather basic information about the bot, including:
   * Bot Name
   * Greeting
   * Main Menu Options
   * Let’s name our Einstein Bot OMC and select the bot’s default language. 
5. Set up a menu for your customers with common issues or questions you want your bot to handle. Let’s enter Order Related in Menu Item 1 for any questions related to a customer’s order. Let’s add Appointment Related in Menu Item 2 for any questions related to scheduling.
6. Click Proceed to build your bot. 


## Chat Bot Message Setup

Now that you’ve built your bot, In the Einstein Bot Builder overview page. It includes the bot’s name and description, a place to train your bot to recognize what customers want, and settings that let you customize the bot response delay time. Click the dropdown arrow symbol and select the Overview page.

To store chat transcripts (including customer data) in the conversation log, click the pencil icon next to Log Conversations. Select Store Einstein Bots conversation data, and click the check mark to save.

To connect the bot to chat deployment click on Add at connections and select the values from the dropdown as Dialogs, Entities and Variables.


Dialogs are conversation snippets that control what a bot can do.
Click Welcome on the left side menu.

Messages—communicate information to the customer using text. If user want to edit the message, click on the message, then at the right side user can see a pencil icon, click on that. In this way you can update your message.
1. Step1: Click on the message/script
2. Step2: At the right side of the page, user can see a pencil icon, click on that.
3. Step3: Update your message.

   * Questions—ask for customer input and store that information.
   * Actions—access Salesforce automation tools such as Apex code, Flows, outbound email, or Object Search.
   * Rules—add conditional logic based on customer data and perform actions such as transfers, setting variables, or ending the chat.

Create a dialog step of each type to review the features in more detail, and use the icons in the top right to clone or move dialog steps. Click the X on each dialog step to remove it. Your dialog should only have the original message dialog step for this project to move forward.
We won't check any of your setup. Click Verify Step to go to the next step in the project.

### Add Pre-built Dialogs To The Main Menu

For the rest of this project, we use the Einstein Bot Builder to set up dialogs, variables, and entities. These are the elements that manage the interaction between your customers and the bot.
Now, let’s update our main menu by adding Recent Orders and Transfer to Agent.
Click Main Menu. This is the Main Menu dialog. It consists of the menu options we specified in setup. Ensure Show a menu is selected. 

1. Click in the Select menu items search field.
2. Select Transfer to Agent.
3. Click in the field again and select Recent Orders.
4. Click Save, which is at the top right of the page.


### Add a New Dialog to the Main Menu
Earlier we added prebuilt dialogs to the main menu. Let’s now add a new dialog.
1. On the Dialogs page, click Deactivate.
2. Click Yes.
3. Click the plus sign and select New Dialog. 
4. Enter Name.
5. Enter API Name.
6. Leave Dialog Description blank.
7. The Assign to Dialog Group setting lets admins group similar dialogs together in the Bot Builder for easy navigation. For now, leave it set to none.
8. Select Show in Bot Options Menu.
9. Click Save.
10. Click Main Menu.
11. In the Next Step section, ensure Show a menu is selected.
12. Click in Select menu items and click the iteam.
13. To rearrange menu items, simply click and drag them to the desired position. Click and drag the item, moving it under other item.
14. Click Save.

### How to Add chatbot to any websites

Step1: Click on setup.
Step2: Type and select ‘Embedded service deployments

Step3: Click on the options from the right portion of the service.
Step4: Select View

Step5: Click on Get Code option.


Step6: From here you can copy the code.


Code Scripts : Add the below code scripts in header and meta tags of any website page

```javascript
<style type='text/css'>
        .embeddedServiceHelpButton .helpButton .uiButton {
                background-color: #005290;
                font-family: "Arial", sans-serif;
        }
        .embeddedServiceHelpButton .helpButton .uiButton:focus {
                outline: 1px solid #005290;
        }
</style>

<script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type='text/javascript'>
        var initESW = function(gslbBaseURL) {
                embedded_svc.settings.displayHelpButton = true; //Or false
                embedded_svc.settings.language = ''; //For example, enter 'en' or 'en-US'


                //embedded_svc.settings.defaultMinimizedText = '...'; //(Defaults to Chat with an Expert)
                //embedded_svc.settings.disabledMinimizedText = '...'; //(Defaults to Agent Offline)


                //embedded_svc.settings.loadingText = ''; //(Defaults to Loading)
                //embedded_svc.settings.storageDomain = 'yourdomain.com'; //(Sets the domain for your deployment so that visitors can navigate subdomains during a chat session)


                // Settings for Chat
                //embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
                        // Dynamically changes the button ID based on what the visitor enters in the pre-chat form.
                        // Returns a valid button ID.
                //};
                //embedded_svc.settings.prepopulatedPrechatFields = {}; //Sets the auto-population of pre-chat form fields
                //embedded_svc.settings.fallbackRouting = []; //An array of button IDs, user IDs, or userId_buttonId
                //embedded_svc.settings.offlineSupportMinimizedText = '...'; //(Defaults to Contact Us)


                embedded_svc.settings.enabledFeatures = ['LiveAgent'];
                embedded_svc.settings.entryFeature = 'LiveAgent';


                embedded_svc.init(
                        'https://appistokisingaporepteltd2-dev-ed.my.salesforce.com',
                        'https://sgb2bcommerce-developer-edition.ap27.force.com/omc',
                        gslbBaseURL,
                        '00D5j000006yS7k',
                        'OMC',
                        {
                                baseLiveAgentContentURL: 'https://c.la2-c2-ukb.salesforceliveagent.com/content',
                                deploymentId: '5725j000000H0bH',
                                buttonId: '5735j000000H1Hy',
                                baseLiveAgentURL: 'https://d.la2-c2-ukb.salesforceliveagent.com/chat',
                                eswLiveAgentDevName: 'EmbeddedServiceLiveAgent_Parent04I5j000000CeLaEAK_17faba8820e',
                                isOfflineSupportEnabled: false
                        }
                );
        };


        if (!window.embedded_svc) {
                var s = document.createElement('script');
                s.setAttribute('src', 'https://appistokisingaporepteltd2-dev-ed.my.salesforce.com/embeddedservice/5.0/esw.min.js');
                s.onload = function() {
                        initESW(null);
                };
                document.body.appendChild(s);
        } else {
                initESW('https://service.force.com');
        }
</script>
``` 

Meta Tag Code Snippet :
```html

<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
```