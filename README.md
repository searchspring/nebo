# slackbot-go

Say hello to Nebo (Nebulous Cloud Being)

<img style="border-radius: 20px; box-shadow: 3px 3px 5px 0px rgba(173,154,173,1);" src="https://www.gravatar.com/avatar/1abed234f87b8153b2cda61601fbb1f9.jpg">

Nebo is a slackbot that helps us ask salesforce questions without having to go into salesforce.

## Usage

`/rep shoes.com`
`/rep bigcommerce`
`/feature i want this feature please`

## Development

### Prereqs
- Install Go https://golang.org/doc/install
- Install Node https://nodejs.org/en/download/
- Install now `npm install -g now`
- Install ngrok `npm install -g ngrok` (because we were too lazy to mock things)

### Run locally

- Create a .env file for local development
 
    ```properties
    SF_URL=https://<your url>.my.salesforce.com
    SF_USER=<sf login email>
    SF_PASSWORD=<sf password>
    SF_TOKEN=<sf token>
    SLACK_VERIFICATION_TOKEN=<slack token>
    ```

- Run the server `now dev`

- Run ngrok `ngrok http 3000`

- Modify your slash command in slack to point at the URL generated by ngrok in the step above.