# Weather App Chrome Extension

Weather App inside a Chrome Extension, Along with Details on How to Create a Chrome App.
<img width="1628" alt="Screenshot 2021-11-24 at 11 52 05 PM" src="https://user-images.githubusercontent.com/49464941/143293929-4aca5b25-4c3c-428e-86eb-0704cb605a61.png">

Follow Step 3 Below to Test this Particular Weather App: https://github.com/pavan-98/chromeweatherapp#step-3

## Creating a Chome Extension App

hrome web apps are extensions or little web elements to run specifically on Google Chrome browsers only. This article is a step by step tutorial for creating a Google Chrome app from your web application which you can use personally or publish it on the Chrome store.

### Step 1

- Create a "manifest.json" file

- In an empty directory, create a manifest.json file at the root of your project. For Manifest V3, the contents should look like this:

```json
{
  "manifest_version": 3,
  "name": "Weather App",
  "version": "1.0",
  "description": "This is a weather application",
  "action": {
    "default_icon": "icon.png",
    "default_popup": "popup.html"
  },
  "icons": {
    "128": "icon.png"
  },
  "content_security_policy": {
    "extension_pages": "script-src 'self'; object-src 'self'"
  },
  "permissions": ["activeTab"],
  "host_permissions": ["https://api.openweathermap.org/*"]
}
```

- _name is the field describing name of your application_

- _version can be any version number of your application._

- _manifest_version is self explanatory which currently is 2._

- _description is the field having the description of your app in 132 characters or less._

- _app:launch:local_path contains the local path from this file to your index file._

- _icons gives path of the icon._

### Step 2

- Create an “icon.png” file
- Icon file is the a file which acts as an image alongside your app name.

- This image is rendered everywhere on google chrome where your application is being rendered like chrome store, your chrome app library, application shortcuts on chrome dashboard,etc.

- This can be of 128*128, 48*48 or 16\*16 or all of these in dimension.

- Details of this file is given on image field of your manifest.json file which is “icons”{“128”:”iconFileName.png”} where 128 tells the dimensions of the icon file and “iconFileName.png” contains the local path from your manifest file to the icon file.

### Step 3

- Test your app

- To test your Google chrome application on your local machine you will need to have Google chrome browser installed on your machine. To start testing:
  Open your chrome browser and select the customize and control Google chrome button present right to the address bar of your browser.

- Then from the left side nav select the Extensions tab.

- Then turn on the developer mode by checking the Developer mode checkbox.

- Click the Load Unpacked Extension button and select the folder of your project containing your project elements,manifest.json file and icon.png .

- Now your application is loaded to test it click on the Apps button underneath the address bar of your browser which will open your app library.

- If everything is right your application should be present in this library. Click on it and test it.
