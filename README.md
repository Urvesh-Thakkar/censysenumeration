- Clone this repo
$ git clone https://github.com/Urvesh-Thakkar/censysenumeration
- Install dependencies
$ pip install -r requirements.txt
- Get Censys API ID and Censys API secret by creating a account on `https://censys.io`

- Add Censys API ID and Censys API secret as  `CENSYS_API_ID` & `CENSYS_API_SECRET` respectively to the OS environment variables. On Linux you can use a command similar to following to do this :

Open Terminal 
Type gedit /etc/bash.bashrc
Add the follwing lines at the end : 

export CENSYS_API_SECRET="<your api secret that you got from your censys account>"
export CENSYS_API_ID="<your censys api id>"



- Check help menu
$ python censys_enumeration.py --help                                                                                                 
Usage: censys_enumeration.py [OPTIONS] FILE

Options:
  --verbose                       Verbose output
  --subdomains / --no-subdomains  Enable/Disable subdomain enumeration
  --emails / --no-emails          Enable/Disable email enumeration
  --help                          Show this message and exit.
  
  
Usage :=

- Subdomain and email enumeration
$ python censys_enumeration.py domains.txt

- Only subdomain enumeration
$ python censys_enumeration.py --no-emails domains.txt 

- Only email enumeration
$ python censys_enumeration.py --no-sudomains domains.txt 

- Verbose output
$ python censys_enumeration.py --verbose domains.txt 

- Output to custom file
$ python censys_enumeration.py --verbose --outfile results.json domains.txt 
