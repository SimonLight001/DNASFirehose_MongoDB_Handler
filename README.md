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

Then I would suggest confirming whether you are an EU or IO customer.
You can tell this by which DNA Spaces domain you connect to https://dnaspaces.eu/ or https://dnaspaces.io.
If you are IO, please scroll through index.py, and change any refernce of .eu to .io.
I have commented on all so shouldnt be too taxing.
E.G. ![image](https://user-images.githubusercontent.com/14348411/129179422-55efbad3-7886-4247-9f53-51945c136746.png)

We then need our activation token from the DNA Spaces Partner platform.
This is found when activating an 'app' in DNA Spaces Partner Dashboard.
We wont use this until we run the script for the first time, so just hold onto it for now.
See screenshot below for more details.
![image](https://user-images.githubusercontent.com/14348411/129176777-877b3b65-f346-49fe-b251-0e81a84eeeac.png)

You will also need a connection to a MongoDB Atlas account.
You can find this by hitting "connect" on your DB, then "Connect your application".
This will give you a URL you need to call to.
Paste this in as CONNECTION_STRING.
Again see the screenshots below for more details.
![image](https://user-images.githubusercontent.com/14348411/129177683-88f8127f-2e95-45a8-a335-3376877904f0.png)
![image](https://user-images.githubusercontent.com/14348411/129177768-5324082b-8c69-4e01-8d31-44b03f37e7b6.png)
![image](https://user-images.githubusercontent.com/14348411/129177803-091daf24-cab5-45ad-bf85-44ca3f4f349d.png)
![image](https://user-images.githubusercontent.com/14348411/129177875-c04f3355-7791-48ac-9d4d-1b1e0394679d.png)
Obviously in this scenario, please fill in the pass with the one yopu just created.

Once this is done, simply run the index.py with 'python3 index.py'.
Firstly it will check to see if an API key already exists.
Assuming this is the first time you are running this file, it will not.
NOTE: If you ever want to change your API key, delete the contents of API_KEY.txt and run index.py again.
If no key exists, it will ask you to enter your activation token.
This is what we copied earlier, so paste in and hit enter.
![image](https://user-images.githubusercontent.com/14348411/129178395-3acae65f-e5e4-4052-b4d6-e8e98f15f47d.png)
The key will then be authenticated, and in doing so your 'app' will become activated in DNA Spaces.
![image](https://user-images.githubusercontent.com/14348411/129178609-4fe8a08a-f7a8-44aa-8174-8764b8ff08c6.png)
![image](https://user-images.githubusercontent.com/14348411/129178685-c65e8630-1b56-431c-991c-192b9d63940b.png)
This will also save your API key in API_KEY.txt.
NOTE: Your activation token and your API key are different things, an API key can be used over and over, and is how we get data from Spaces. An activation token is used once, and is how we activate an app in DNA Spaces, and how we get an API key.

From this point, data should start flowing in:
![image](https://user-images.githubusercontent.com/14348411/129179020-0a4493fa-788a-4e27-92c3-c7f079ba4041.png)
For debugging purposes, uncomment some of the prints in the bottom of the index.py to see what data is being sent.
![image](https://user-images.githubusercontent.com/14348411/129179090-6c6ec875-8d5e-4027-93de-370581443dc9.png)


[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/SimonLight001/DNASFirehose_MongoDB_Handler)
