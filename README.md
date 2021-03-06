# stay-posted
Sends free postcards using the PoscardCreator App from the Swiss Post. Supports multiple accounts. 

## Setup

You need the following folder structure in order to have a functioning script.
To achieve this structure just activate the setup.py script, add images to new and you will automatically send postcards to yourself. To adjust this just change the config/setup.json
<pre>
stay-posted/
├── config
│   ├── accounts.json
│   └── setup.json
images/
├── images
│   ├── new
│   │   ├── Images.jpg
│   │   └── to_send.jpg
│   └── sent
│       ├── all.jpg
│       ├── sent.jpg
│       └── images.jpg
├── logs
│   ├── error.log
│   └── stay-posted.log
├── README.md
├── requirements.txt
└── stay_posted.py
</pre>
### Requirements
All requirements are listed in the requirements.txt file

### Config Files
accounts.json:
<pre>{
  "accounts": [
    {"user": "email",  "pwd": "password"},
    {"user":"email", "pwd":"password"}
    ...
  ]
}</pre>

setup.json:
<pre>{
  "sender": {
    "prename": "your_prename",
    "lastname": "your_lastname",
    "street": "your_street_and_number",
    "place": "your_city",
    "zip_code": 1234
  },
  "recipient": {
    "prename": "recipient_prename",
    "lastname": "recipient_lastname",
    "street": "recipient_street_and_number",
    "place": "recipient_city",
    "zip_code": 1234
  },
  "message": "your_message"
}
</pre>

## Credit
This script uses the [postcard-creator-wrapper](https://github.com/abertschi/postcard_creator_wrapper)
