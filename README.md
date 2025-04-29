:exclamation: draft :exclamation:

# Commerce Partner Days - ACCS Session

https://github.com/rojoangel/extensibility-lab

## CLI / Scaffolding

1. Visit https://github.com/rojoangel/extensibility-lab
2. Navigate to the top right of the page and click on the `Use this Template` button. Select the `Create a new repository` option to create a new repo with the template. <img width="1701" alt="image" src="https://github.com/user-attachments/assets/63ef2b17-bf03-4e3c-848f-6d990c492261" />
3. This should launch the repo provisioning UI. Select your personal account as the owner and enter an appropriate name for the repo. Make the repo `Private` and click on `Create Repository` to create create a repo from the template. <img width="881" alt="image" src="https://github.com/user-attachments/assets/aabc8b22-1ba3-4058-af6b-2f70ec505d0c" />
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
10. Now lets connect the terminal to your assigned Adobe IMS account.

TBD

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

# Commerce Partner Days - ACO Session

TBD
