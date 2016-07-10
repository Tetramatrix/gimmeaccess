"Gimme access to your Dropbox account"

1. What is does it do?
This script authorize other Dropbox users and creates a bearer to use your app (Dropbox v2.2 app authorization for other users).

1.2. Features
- Dropbox v2.2
- PHP5 (no cUrl needed)
- tiny
- Screenshot (gimme.png)
- implicit grant

2. Requirement
2.1 Dropbox account
2.2 appkey and secret
2.3 PHP5
2.4 Webserver

3. Installation
3.1 Download appkeys.php,dropbox.php,gimme.html,http.php,oauth_client.php,oauth_configuration.json,readme.txt to a folder in your webserver.  Make sure the folder is not in a private network and accessible to the Dropbox site.
3.2 Edit appkeys.php and update $appkey and $secret to match your appkey and secret. 
3.3 Edit dropbox.php and update $client->redirect_uri (Callback Url) to match your webserver and point to grant.php. Make sure this URL is not in a private network and accessible to the Dropbox site.

4. Tutorial
4.1 In webbrowser open gimme.html and press button "Gimme access to your Dropbox account".
4.2 Authenticate the app with the users Dropbox account credentials.
4.3 After authenticate the webbrowser is redirected to the callback uri with a document showing the bearer of the user.

5. Troubleshooting
5.1 Callback uri has to be registered to the dropbox api
5.2 After authenticate the redirect should look like this: 
https://localhost:8080/grant.php#access_token=Kj25mwyQeqAAAAAAAAAD-bJA5dnRK6VZXsonHBWbkLEKKhRAglTmE7VQ8F6LiXxT&token_type=bearer&state=1468088355-1f829e&uid=888888888&account_id=dbid%3AAABAylxMQai_2WmEbFoz6zISPFzjWbM4o10
5.3 gimme.png shows a screenshot after pressing "Gimme access to your Dropbox account"
5.4 It uses implicit grant so need to convert authorization code to bearer!

6. Changelog
Initial release

7. Thanks to Manuel Lemos from phpclasses.org for Oauth (http://www.phpclasses.org/oauth-api) and http client (http://www.phpclasses.org/httpclient). 