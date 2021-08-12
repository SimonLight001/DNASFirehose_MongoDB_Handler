# DNASFirehose_MongoDB_Handler

This file is designed to create a simple interface between DNA Spaces Firehose stream, and MongoDB Atlas.

For those of you who are using a .io domain, please make sure you manually change domains.
This will be something I will add in the future, that domain will be held as a single variable.

If you have any questions or need help using the script please reach out!



![image](https://user-images.githubusercontent.com/14348411/128566457-8de0e8c7-dc33-4931-929b-553d124cd27b.png)

![image](https://user-images.githubusercontent.com/14348411/128566477-3a23252f-96b4-46f2-8535-554a6d32d946.png)

## How to run

Start by installing all prerequisites.
This can be done using the requirements.txt file.
There are a couple different ways to do this, so please see [here](https://pip.pypa.io/en/stable/cli/pip_install/#example-requirements-file).

We then need our activation token from the DNA Spaces Partner platform.
This is found when activating an 'app' in DNA Spaces Partner Dashboard.
We wont use this until we run the script for the first time, so just hold onto it for now.
See screenshot below for more details.

You will also need a connection to a MongoDB Atlas account.
You can find this by hitting "connect" on your DB, then "Connect your application".
This will give you a URL you need to call to.
Paste this in as CONNECTION_STRING.
Again see the screenshots below for more details.

Once this is done, simply run the index.py with 'python3 index.py'.
Firstly it will check to see if an API key already exists.
Assuming this is the first time you are running this file, it will not.
NOTE: If you ever want to change your API key, delete the contents of API_KEY.txt and run index.py again.
If no key exists, it will ask you to enter your activation token.
This is what we copied earlier, so paste in and hit enter.
The key will then be authenticated, and in doing so your 'app' will become activated in DNA Spaces.
This will also save your API key in API_KEY.txt.
NOTE: Your activation token and your API key are different things, an API key can be used over and over, and is how we get data from Spaces. An activation token is used once, and is how we activate an app in DNA Spaces, and how we get an API key.

[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/SimonLight001/DNASFirehose_MongoDB_Handler)