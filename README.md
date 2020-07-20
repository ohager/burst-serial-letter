# burst-serial-letter
A small tool to send Burstcoin messages in masses

## Installation

> You need Nodejs (Version >=14) installed

`npm i burst-serial-letter -g'

Now it should be available as CLI command, type:

`burst-serial-letter --version` 



## Usage 

The tools comes with its built-in help. 

Just type `burst-serial-letter -h`

Before you can send data you need to prepare a json file to set up
the Burst Node, the message and the recipient list.

Create a Json file, e.g. `my-message-info.json` with the following fields:

```json
{
  "host": "https://testnet-2.burst-alliance.org:6876", // use the right host address
  "message": "<Your message here>", 
  "recipients": [
    // add account ids or addresses here
  ]
}
```

Then run `burst-serial-letter -d ./my-message-info.json`

Keep in mind, that sending messages costs you BURST. 
So, better to test your serial letter on testnet before. 
You can/should even run a dry run, without actually sending the messages using the `--test` flag:

`burst-serial-letter -d ./my-message-info.json --test`

Happy Spamming!
