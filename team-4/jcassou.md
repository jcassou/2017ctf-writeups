# Main Role
- Create a flag updater for Team4's notary

## Notary's flag updater 
- First step of the updater is to daemonize the process : use of fork() function and close STDIN, STDOUT and STDERR
- The second step consist in listening to the client on port 42 to catch flag
- The flag is GPG encrypted, I used a python function (easier than c api) to decrypt it
- I parsed manually the JSON file to get the 3 main features, with strtok() function
- This last step gives me an encrypted-64 signature : again I used a python function to decrypt it
- It gives a GPG signature 
- I verified the signature checking who was the signer (if it is a TA, it's good and I copy the flag into /var/ctf, if not, I don't)  
