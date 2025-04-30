:exclamation: draft :exclamation:

# Commerce Partner Days - ACCS Session

https://github.com/rojoangel/extensibility-lab

## Codespaces Setup

1. Visit https://github.com/rojoangel/extensibility-lab
2. Navigate to the top right of the page and click on the `Use this Template` button. Select the `Create a new repository` option to create a new repo with the template. <img width="1701" alt="image" src="https://github.com/user-attachments/assets/63ef2b17-bf03-4e3c-848f-6d990c492261" />
3. This should launch the repo provisioning UI. Select your personal account as the owner and enter an appropriate name for the repo. Make the repo `Private` and click on `Create Repository` to create a repo from the template. <img width="881" alt="image" src="https://github.com/user-attachments/assets/aabc8b22-1ba3-4058-af6b-2f70ec505d0c" />
4. Congratulations, you now have the tools to create and extend your own commerce store.
5. Click on the `Code` icon and select the `Codespaces` tab. Click on the `+` icon to create a new personal codespace. <img width="1497" alt="image" src="https://github.com/user-attachments/assets/d060f11e-197f-44c6-9f68-2274c2ba22d6" />
6. This will launch a new codespace on the repo. The initialization will take around 3-4 minutes. <img width="731" alt="image" src="https://github.com/user-attachments/assets/d4e18627-2fed-47b5-b8cc-ea3b0b2743f7" />
7. Once done, you will be able to interact with the online IDE. <img width="2007" alt="image" src="https://github.com/user-attachments/assets/96c71fab-b179-442f-8378-9203d4facd83" />
8. Navigate to the terminal and run the following command to clear the temporary github token:
```bash
unset GITHUB_TOKEN
```
9. Now lets connect the terminal to your personal Github account. Run the following command:
```bash
gh auth login
```
This should launch the login process. Select the appropriate options to log into your Github account.

<img width="686" alt="image" src="https://github.com/user-attachments/assets/d15dc8ba-febe-461d-9117-4ba16026e7ed" />

Once done you should see the following on the login screen:

<img width="1255" alt="image" src="https://github.com/user-attachments/assets/3678bc9c-cd52-4505-8c7b-6514731e1a33" />

10. Now lets connect the terminal to your assigned Adobe IMS account. Run the following command in the terminal:
```bash
aio auth login --force
```
If you are asked to confirm your action to open an external website, click `Open`.
<img width="1402" alt="image" src="https://github.com/user-attachments/assets/dcbc0ad7-b1e1-499a-ac95-3edf6fb97a35" />

Enter your email ID in the following format: `pd-sj+<SEAT_NUMBER>@adobeevents.com`. You will find your assigned seat number on your desk.

<img width="1448" alt="image" src="https://github.com/user-attachments/assets/33db1f73-837f-4d6e-a6b1-2ce732638cfd" />

Enter the following as password: `TBD`

<img width="1503" alt="image" src="https://github.com/user-attachments/assets/c7bd6155-dce2-4c4d-8ca4-24881e0a327e" />

Once login is successful, you will see a redirect link, click on it

<img width="919" alt="image" src="https://github.com/user-attachments/assets/ff643d9e-5fdc-4b71-b847-de1b175f113b" />

You will see an error such as this:

<img width="920" alt="image" src="https://github.com/user-attachments/assets/b9f38524-3292-49a3-95dc-cedc89124ed0" />

No worries, make a note of the port number in the address bar, for instance:

<img width="1022" alt="image" src="https://github.com/user-attachments/assets/4e88cc88-47bb-479b-8583-d2954ce43260" />

Go to the ports tab next to the terminal in the Codespaces window

<img width="1663" alt="image" src="https://github.com/user-attachments/assets/4be13b53-12d8-4336-9536-f6252eff8fee" />

Look for an auto-forwarded port with the same port number as earlier from the error window. Once you identify the appropriate forwarded port, copy it.

<img width="1562" alt="image" src="https://github.com/user-attachments/assets/408747c6-0389-4d0f-8749-ae309bcccdc8" />

Navigate back to the error window and replace `127.0.0.1:<PORT_NUMBER>` with the copied text, and click enter. This will connect the IMS login on the browser to the Codespaces terminal.

<img width="936" alt="image" src="https://github.com/user-attachments/assets/019f8f26-2be2-41e8-b6b1-279e4e20dba2" />

## Create Storefront

Congratulations on creating a codespace and completing the pre-requisite steps. Now comes the fun part, lets create a storefront and connect it to a Commerce instance using API Mesh.

1. Run the commerce scaffolder CLI
```bash
aio commerce init
```
2. Make sure the CLI has selected the right github account. If so, Enter `y`.
3. Enter a name that will be used as the name the storefront repo. Make sure it isnt used in the past.
4. Select the first template in the list `adobe-commerce/adobe-demo-store`
5. Select the second option, which will allow us to select an assigned instance `Pick an available Adobe Commerce tenant`
6. This will prompt us to select the Org. Select the following org `TBD` and enter
7. From the list of instances, select the instance assigned to you. You can search for your instance by typing `Cloud Service <SEAT_NUMBER>`
8. From the list of projects, select the project assigned to you. You can search for your project by typing `TBD`
9. Select the Production workspace
10. This will connect the selected instance through an API Mesh on the selected Project and Workspace
11. In the next step if a browser tab isnt opened, go to this link https://github.com/apps/aem-code-sync/installations/select_target
12. Select the appropriate account to install the AEM Sync Bot and complete the login process if any
13. Select the option to only install on selected repositories. Enter the name of the repo from 2nd question in the dropdown and click save.
14. TBD

## Storefront Extensibility (Phase 1)

1. Clone locally
1. Open PDP block
1. Add runtime fetch to mock service for ratings
1. Render response

## Mesh Extensibility (Phase 2)

1. Add mock service as products.ratings schema

## Storefront Extensibility (Phase 3)

1. Update Storefront to use build.mjs to modify pdp schema
1. Use this data somehow, ie via slot context, and remove runtime fetch

## Adobe Commerce Integration Starter Kit (Phase 4)

The purpose of this exercise is to demonstrate sending events from Commerce to Adobe Developer App Builder. You will use a simplified version of the Adobe Commerce Integration Starter Kit to configure Commerce and an App Builder project, allowing for the sending of events about saved orders.

### 1. Configure the Starter Kit

1. Login to the Adobe Developer Console at https://developer.adobe.com/console/ and select the **Commerce Extensibility Lab** organization. 
    
    Developer Console is the gateway to access all the services and tooling available as part of the Adobe Developer Ecosystem, including App Builder. 

    Use the username format:
    
    **pd+sj+\<SEAT_NUMBER\>@adobeevents.com**

1. Select the project assigned to your seat: 

    **Cloud Service <SEAT_NUMBER>**

    *Tip: Use search to find your project*

    Select the **Stage** workspace.

    Download the workspace JSON configuration file by clicking on the **Download all** button on the upper right corner of the page. Save it as `workspace.json` at `extensibility-lab/scripts/onboarding/config/workspace.json`

1.  Copy the `env.dist` file in `extensibility-lab` as `.env` 
    ```bash
    cp env.dist .env
    ```

    Then configure the `.env` file with all the information required:

    - To find the values for the OAuth config variables, click **OAuth Server-to-Server** in the Developer Console Workspace overview page for the Stage workspace.

        ![Alt text](docs/oauth-credential.png "OAuth Server-to-Server Credential")

    - Set the REST endpoint for your ACCS instance as the value for the `COMMERCE_BASE_URL`. The endpoint should be in the following format: `https://na1-sandbox.api.commerce.adobe.com/<TENANT_ID>/`

    - Fill in the `IO_CONSUMER_ID`, `IO_PROJECT_ID`, and values `IO_WORKSPACE_ID` using the downloaded `workspace.json` file and the commented instructions in the `.env` file.

1.	Link the project in the current directory to the project in the Adobe Developer Console by running the following commands in the terminal:

    ```bash
    # force logout 
    aio logout --force

    # login to Adobe I/O CLI
    aio login

    # configure Adobe I/O CLI to use the Commerce Extensibility Lab organization
    aio console org select

    # configure Adobe I/O CLI to use the project assigned to your seat
    aio console project select

    # configure Adobe I/O CLI to use the Stage workspace
    aio console workspace select

    # configure Adobe I/O CLI to use the previous selections for the current project
    aio app use --merge
    ```

1. Install and deploy the application:

    ```bash
    npm install
    aio app deploy
    ```

    Take note of the link to the deployed application in the Experience Cloud shell. This will be used later in the lab.

    ![Alt text](docs/deployed-app-url.png "Application's Experience Cloud shell URL")

    After running the command and clicking the **Runtime** tab in the Developer Console for your Stage workspace, runtime actions are visible.

    ![Alt text](docs/dev-console-actions.png "Runtime actions in the Developer Console")

### 2. Onboarding

The starter kit provides boilerplate code for synchronizing entities across systems and onboarding scripts to simplify setup. During installation, there are low/no manual activities required.

To ensure flexibility for the onboarding scripts, the starter kit code provides a few different JSON configuration files to match your business requirements. All the files were pre-configured for this lab. The most important files are described below:

- `scripts/onboarding/config/providers.json`

  Defines the providers required during the integration. The "key" field will reference the providers in other configuration files. The rest of the fields are descriptive.

  For this specific lab, we will focus on creating a Commerce provider for sending events to App Builder. Although not used for this specific lab, the starter kit also supports creation of backoffice providers for sending information from backoffice systems to Commerce.

- `scripts/onboarding/config/events.json`

  Defines all the meaningful events that the integration needs to care about. For this lab, we'll focus on the `com.adobe.commerce.observer.sales._order_save_commit_after` event listed at the beginning of this file.
  
  If more events were required, we would specify them in this file. Although not used for this lab, the full starter kit also provides support for product, customer, and stock events.

- `scripts/onboarding/config/starter-kit-registrations.json`

  Defines the required event registrations that will be created in App Builder. For this lab, the file has been configured so that only a registration for order events from Commerce will be created. When the registration is created, order save Commerce events will trigger runtime action code that we've added in the `actions/order/commerce` directory to save order data within the App Builder app.

- `scripts/commerce-event-subscribe/config/commerce-event-subscribe.json`

  Defines the event names and fields that must be subscribed to in Adobe Commerce. Information for the `com.adobe.commerce.observer.sales._order_save_commit_after` that will be used in this lab is provided in this file.

Now it's time to realize the onboarding. Go to your terminal and run the following commands:
```bash
npm run onboard
```

After successfully running this command, an event registration within your Stage workspace will be visible in the Developer Console.

![Alt text](docs/workspace-overview-registration.png "Workspace overview with event registration")

![Alt text](docs/registration-details.png "Event registration details")

Then, to automatically subscribe to the order save Commerce event, go to your terminal and run
```bash
npm run commerce-event-subscribe
```

### 3. Send information from Adobe Commerce to App Builder

Navigate to the link for the deployed application in the Experience Cloud shell that was included in the console output after running the `aio app deploy` command. The application contains a single page UI with a panel labeled **Latest Orders Received**. The panel is initially empty, but a grid with information about saved orders will appear after Commerce order save events are received and saved by the App Builder app's runtime action. The grid refreshes at regular intervals, allowing for the display of new order information.

In the storefront for your Commerce instance, place at least one order. After Commerce order save events are received in App Builder, the panel in the app's UI will look similar to the following:

![Alt text](docs/order-grid-ui.png "Application UI Order Grid")

This demo App Builder app simply stores and displays received order information, but the action code for the app could also be modified to send information received from Commerce to a third-party back office system. Although not shown in this demonstration, the starter kit can additionally be used in setting up the synchronization of data from third-party back office systems to Commerce.

# Commerce Partner Days - ACO Session

TBD
