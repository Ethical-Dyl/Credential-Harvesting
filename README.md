# Credential-Harvesting
This is a writeup on how to use the popular tool SEToolkit to harvest credentials.


# Firing up the toolkit

This toolkit must be run as root:

Syntax: "sudo setoolkit"

 After entering the syntax to fire up the toolkit it can be seen there are seven different options for us to choose. For this writeup I will be using #1, Social-Engineering Attacks:
 
 <img width="458" alt="image" src="https://user-images.githubusercontent.com/66540055/194626715-5360e227-6810-4936-93ff-6d68c9c4472f.png">
 
 After the selection has been made there will be eleven options to be selected from, I will be selecting #2:
 
 <img width="472" alt="image" src="https://user-images.githubusercontent.com/66540055/194627146-353d8b32-a3f3-42a1-bba9-f22b1ecfe10d.png">


After the selection has been made another prompt will ask which web attack module is to be used, I will be selecting #3:

<img width="402" alt="image" src="https://user-images.githubusercontent.com/66540055/194627479-d6878851-dabf-4014-96e8-f580399ee534.png">


After the selection has been made there will be four options to be chosen, I will be selecting #2 Site Cloner and enter the following:

<img width="427" alt="image" src="https://user-images.githubusercontent.com/66540055/194628646-c2004c72-b85a-4da9-8c95-af1bc559d6e8.png">

Adding the site to clone:

<img width="838" alt="image" src="https://user-images.githubusercontent.com/66540055/194636341-8380456c-3d64-4c0e-a391-3dccb2bb067f.png">

Now that the toolkit is running on port 80, I will verify that it is indeed running by navigating to it on another computer:

<img width="665" alt="image" src="https://user-images.githubusercontent.com/66540055/194637017-e8127f16-bb4b-43a3-aa02-f6bbffc869d1.png">

# Harvesting Credentials

Now that I know the service is running, I will enter in some credentials to harvest:

Here is what is being entered from the victim side:

<img width="388" alt="image" src="https://user-images.githubusercontent.com/66540055/194637507-8ebe533c-943c-4e13-94b4-14ef6e7864f8.png">

After entering the credentials, the toolkit forwards the victim to the real Facebook login site, making it seem as though the login attempt didn't successfully go through! See below:

<img width="705" alt="image" src="https://user-images.githubusercontent.com/66540055/194638043-b73eaec0-9de5-48c9-9190-03ce964ffd01.png">


Here is what is seen on the attacker side:

<img width="468" alt="image" src="https://user-images.githubusercontent.com/66540055/194637652-4b244c47-6ccf-48d7-b640-6dbce8a48f3c.png">

As it can be seen, if this was a real attack the hacker would now have the user's credentials.

# Final Thoughts

It is important to take steps to ensure that any and all requests being made from your computer are going to an authentic site, one key indicator to seeing if a site is authentic is looking at the certificate issues like below:

<img width="957" alt="image" src="https://user-images.githubusercontent.com/66540055/194638694-9455ec72-da89-42c1-a45a-cb26435a7014.png">


You may be thinking, well another clear indicator is that the URL above is an IP address and not the usual www.facebook.com. That is a correct oberservation but that can easily be spoofed by tampering with the host file on the machine or the DNS server in the network. I will be going over pharming attacks more in-depth in due time. 

Thanks for reading, Happy Hacking!
