### Introduction
For this project, you will need to make an Android application to create a
contact and dialog with SMS.

The goal here is to understand how an Android application works, how
Android manages your application and how to use the SDK.

### Goals
You will have to perform various tasks that will make you understand how
an Android application in JAVA or Kotlin. The goal is to have an application that allows
so much to create a contact (with at least 5 informations), to edit it and to delete it.
Once registered contact it will be possible to dialogue with him using the
SMS.

Contacts are persistently saved (SQLite database, do not use
not the shared contact table, but create your own). A summary of each contact
will be present on the application home list, a click on a summary
will see all the information about the corresponding contact.

Your application will also have to work in two languages, one of which is default
(change the language of the system to test). When you are on the home and you
pass the application in the background, the date will be saved and displayed in a toast when
of your return to the foreground. A menu will change the color of the header of
the application. And finally, the icon of the application will be the logo of 42.

### General instructions
- This project will only be evaluated by humans.
- The project must be in JAVA or Kotlin
- No external library (even for design) is allowed.

It is strongly recommended to use Android Studio as IDE.
Be careful, the ADT plugin for Eclipse is no longer supported by
Google.

### Mandatory part
Here's what you will need to do:
- Creating a contact.
- Editing a contact.
- Deleting a contact.
- Homepage with a summary of each contact.
- Receive SMS from your saved contacts.
- Can send SMS to your contacts.
- A menu must be available to change the color of the header.
- The application will have to support two languages.
- Show the time of the background when returning to the application.
- The application works in portrait and landscape mode.
- The logo of the application will be 42.

### Bonus part
- Have a photo for the contacts.
- On receipt of an SMS, a contact with the number in name is directly created
- It's beautiful ! Material Design is cool.
- We can call the contact.

Indulge yourself, lots of things can improve the application.

### Emulation
This part explains how to use an Android emulator.

The emulator provided with Android Studio does not work for the
moment on the dumps. I invite you to use Android Studio on
a VM or a real device if you want to test SMS.
Several Android emulators exist, some more or less good: GenyMotion is
very powerful and easy to set up (VirtualBox is required) but does not allow
sending SMS in its free version. 
The AVD (Android Virtual Device) that comes with Android Studio is not the most
powerful, but you have control. It is set up alone with Android Studio,
it's intuitive.

To send an SMS from the AVD:

`srudent @ e1r1p1 $ telnet localhost {port, (window title)}`

`#Trying 127.0.0.1 ...`

`#Connected to localhost.`

`#Escape character is '^]'.`

`#Android Console: type 'help' for a list of commands`

`#OK`

`sms send {number} {message}``

For a call:

`srudent @ e1r1p1 $ telnet localhost {port, (window title)}`

`# [...]`

`gsm call {number}`

When an image is running, the computer recognizes it as a fax.
phone. Just choose the image when you launch the application from Android
Studio.

### Rendering and peer-evaluation
Be careful with your deposit, full of more or less useful files are generated in your
project. Remember to set up your .gitignore hint.
For the correction the project will be compiled and installed with:
`$. / gradlew installDebug`
