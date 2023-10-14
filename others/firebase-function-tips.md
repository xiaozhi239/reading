Firebase cloud function wraps on top of GCP cloud functions.

Firebase cloud function [Quirks](https://www.youtube.com/watch?v=rERRuBjxJ80):
* Cloud function will have **cold startup** to load the deps and set up the env the first time. The more frequent and stable the calls, the faster they are.
* Each cloud function runs in its **own container**, no matter if you write them into one file. So be careful about global variable might not work the way you thought. 
* Every global variable (including `import`) will be **loaded in every cloud function** container, no matter whether or not they need it. So making sure heavy loading should be loaded lazily inside cloud functions.
* functions sometimes can be called **more than once** for the same event. You could rely on context.eventId - they will be the same for the same event. Watch out for it, especially for things like **payment**.
* By default, cloud function terminates after running for 1 min. You could increase it up to 9 minutes.

Cloud firestore limits to 1MB max per document. 




