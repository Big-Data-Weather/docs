# What this software must do

Quotaero

Jeffrey Fellows, Rebecka Goncharov, Ronnie Nguyen, Bradley Cruce,John Delshadi, Steven Ov

##INSTRUCTIONS##
The file should have three sections. The first section should be called “Assumptions.” The second should be called “Functional requirements.” The third should be called “Non-functional requirements.” The document should be no more than 1000 words. Write your “assumptions” section last. The document will be graded on how comprehensively and clearly it specifies what your system must do.

## Assumptions

The user will have:

+ a browser that supports HTML5 and JavaScript
+ a broadband internet connection
+ a relatively fast computer
+ a mouse

The user will not be red-green colorblind. The currently proposed color palette is not colorblind-safe. We will develop a colorblind-safe color palette in the next version.

## Functional requirements

### User account requirements

#### Account creation

+ The system shall allow a user to create an account.
+ When creating an account, the system shall require the user to enter a valid email address and a password.
+ The system shall obscure the password as the user enters it.
+ The system shall require the user to enter the password twice (to "confirm" it).
+ If the user enters a string that cannot be a valid email address in the email address field, the system shall tell the user they have done this and prompt them to enter a valid email address.
+ The email address must be unique. If the user enters an email address that corresponds to an already existing user account, the system shall tell the user this and prompt them to enter another one.
+ If the user enters different strings in the "password" and "confirm password" fields, the system shall tell them they have done this and prompt them to make the two fields match.
+ If the user submits a unique and valid email address and the "password" and "confirm password" fields match, the system shall create the account, log the user in, and send a confirmation email to the email address.

#### Password management

+ The system shall allow the user to reset their password without logging in. The system shall generate a new password and email it to the email address associated with the account. This email should instruct the user to change their password after logging in with the system-generated password.
+ The system shall allow the user to change their password once they have logged in.

#### Account deletion

+ The system shall allow the user to delete their account.

### Interface requirements

+ The system shall store two classes of simulated squirrel populations: public and private. Public populations shall be viewable by any user without logging in. To take actions within a public population, however, the system shall require a user to log in. Private populations will be accessible only to their "owners".
+ The system shall allow a logged-in user to take the following actions on simulated squirrel populations:
  + create (public or private)
  + destroy (if the logged-in user is the owner)
  + add manager
  + view statistics
  + change environment parameters
+ The system shall associate an amount of "energy" with each user account.
+ The system shall "charge" the logged-in user a fixed amount of "energy" for actions that change the enviroment (e.g., changes to environment parameters).
+ The system shall allow the user to visualize the squirrel population in its environment.
+ The system shall allow the user to see attributes and life histories of a particular squirrel in a given population.
+ The system shall allow the user to name individual squirrels.
+ Once a squirrel is named, the system shall prevent the user from changing the squirrel's name.

## Non-functional requirements

+ No system action shall take more than 5 seconds to complete.
