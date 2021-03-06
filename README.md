
  
# vue-gapi-example    
 [![npm](https://img.shields.io/npm/v/vue-gapi.svg)](https://www.npmjs.com/package/vue-gapi) ![vue2](https://img.shields.io/badge/vue-2.5.x-brightgreen.svg) ![vue2](https://img.shields.io/badge/vuetify-1.3.x-brightgreen.svg) ![license](https://img.shields.io/badge/license-MIT-green.svg)  

> Example application how to use the vue-gapi plugin. The application uses Vuetify.      
 ## Setup        
 #### Google API        
 To use this example application you must register the application in the [Google API Console](https://console.developers.google.com/).         
        
1. Go to the [Google API Console](https://console.developers.google.com/).        
2. From the project drop-down, select an existing project or create a new one by selecting `Create a new project`.        
3. In the sidebar under `APIs & Services`, select `Credentials`, then select the `OAuth consent screen` tab.      
      
    Choose an `Email Address`, specify a `Product Name`, and press `Save`.        
          
4. In the `Credentials` tab, select the `Create credentials` drop-down list, and choose `OAuth client ID`.      
      
   - Under Application type, select `Web application`.         
   - Register the origins from which your app is allowed to access the Google APIs, as follows. An origin is a unique combination of protocol, hostname, and port, i.e. `http://localhost:8080` for your development machine.      
   - In the Authorized JavaScript origins field, enter the origin for your app. You can enter multiple origins to allow for your app to run on different protocols, domains, or subdomains. You cannot use wildcards. In the example below, the second URL could be a production URL.        
     - http://localhost:8080        
     - https://myproductionurl.example.com        
   - The Authorized redirect URI field does not require a value. Redirect URIs are not used with JavaScript APIs.        
   - Press the `Create` button.        
   - From the resulting OAuth client dialog box, copy the `Client ID`. The `Client ID` lets your application access enabled Google APIs.      
      
5. In the `Credentials` tab, select the `API key` drop-down list. Copy the `API key` from the dialog box. The `API key` lets your application access enabled Google APIs without authorization.      
6. In the sidebar under `APIs & Services`, select `Library`, then enter `Calendar` in the search field. Click on Google Calendar API and in the next screen click the `Enable` button.      

> IMPORTANT
> This is the simple setup. When moving to production make sure you set restrictions on both the API Key and OAuth Client ID to avoid misuse of your API Key and Client ID! I strongly advise you to restrict use to explicit domains and for specific APIs. You have been warned :-)
  
#### Create .env.local file        
 Add the API Key and Client ID you created in the previous step to the file .env.local in the root directory of the project.

> NOTE
> Please note that the prefix VUE_APP_ is mandatory for Vue to pick op the settings in the .env.local file.     
 
- Rename the .env.local.tpl file to .env.local  
- Add your API Key and Client ID to the entries

  ```
  VUE_APP_GAPI_API_KEY=the-api-key-you-created
  VUE_APP_GAPI_CLIENT_ID=the-client-id-you-created
  ```
 ## Project setup        
 ``` npm install ```        
 ### Compiles and hot-reloads for development        
 ``` npm run serve ```        
 ### Compiles and minifies for production        
 ``` npm run build ```        
 ### Run your tests        
 ``` npm run test ```        
 ### Lints and fixes files        
 ``` npm run lint ```      
 ## To do    
- [x] UI    
- [x] Authentication    
- [x] Offline access token    
- [ ] Accessing Google Calendar
- [ ] Client example offline access token
