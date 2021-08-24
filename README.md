<b>goIndex<b>

### Quick Deployment
1. Open https://install.kenci.workers.dev

2. Complete authorisation and input all the details and generate code

3. Head over to the index.js file and input the client id ,client secret, refresh token and root id from the code generated in step 2

4. Deploy this index.js code to Cloudflare Workers
  
### Manual Method to generate Client ID, Client Secret and Refresh Token (Recommended)

* Open https://console.developers.google.com/apis/credentials
* Create your project if you dont have one!
* Then Search for Google drive Api And Enable it!
* Click create credentials then Select OAuth client ID.
* Select Web application.
* Give it a name. (anything for your own reference)
* In Authorized JavaScript origins add https://developers.google.com
* In Authorized redirect URIs add https://developers.google.com/oauthplayground
* Save and note down your Client ID and Secret And then click on OAuth Consent Screen.
* Click on publish Your App. then Open in new tab https://developers.google.com/oauthplayground
* On Right Top Side click on Setting Icon ![](https://developers.google.com/oauthplayground/assets/images/settings.png)
* Click on Use your own OAuth credentials.
* Enter OAuth Client ID: and OAuth Client secret:
* Now back to same page https://developers.google.com/oauthplayground left side Step 1 i.e. Select & authorize APIs
* Find Drive API v3
* Select First Option i.e. https://www.googleapis.com/auth/drive
* Click on Authorize API. and give permissions using your google account.
* It will turn to Step 2 Exchange authorization code for tokens at the end of authentication.
* Click on Exchange authorization code for tokens, if it goes to step 3, click on Step 2 yourself.
* Select the option Auto-refresh the token before it expires.
* Copy the refresh token and paste in Line 7 of https://github.com/sawankumar/Google-Drive-Index/blob/master/index.js along with your own Client ID and Secret at Line 5 and Line 6 respectively.
* Copy the Code and paste it into https://workers.cloudflare.com Site.

### Credits:
GDindex by: @maple3142
Nexmoe theme by: @5MayRain , Translated by @genos2000
