# CBC Bitflipping Demonstration

A excercise developed to demonstrate a CBC bitflipping attack, which allows modification of information encrypted using Cipher Block Chaining (CBC). A good writeup of the vulnerability can be found at: https://www.arxumpathsecurity.de/blog/2019/10/16/cbc-mode-is-malleable-dont-trust-it-for-authentication

## Explanation
Navigating to the excercise page displays a login form. Entering details into this login form generates an encrypted cookie. This cookie can be submitted back to the application to "login" to it.

However, due to a lack of message authentication by the application, it is possible that a cookie can be crafted and sent to the server by a malicious party in order to bypass authenication or force other behaviour.

There is an admin account present on the application. To access this admin account, a provided cookie must include a special parameter indicating the cookie belongs to an admin account. The objective of the excercise is to gain access to this admin account by modifying a cookie and submitting it to the application.

## Basic approach to completing exercise
1. Play with the username and password and determine the makeup of the cookie which is generated.
2. Craft a new cookie to submit to the application which will allow for admin access.
3. Submit the crafted cookie and get admin.

