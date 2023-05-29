# Convin REST API

The Convin REST API allows clients to send requests to the Convin REST API server. The server will handle authentication by redirecting requests to an OAuth server. Once authenticated, the server will send requests to the Google Calendar API to retrieve events and provide the event list to the client.

Please note that due to verification requirements on the Google Cloud Dashboard, this API cannot be published. To test the API, please provide a Gmail ID so that it can be added as a test user.

The APIs are currently running on Repl.it in a public environment.

# Flowchart
![image](https://github.com/zaidragib1/convin-rest-api/assets/110742924/8a3ddb20-66d3-4d0d-9803-9872b44036e4)

# Response
![image](https://github.com/zaidragib1/convin-rest-api/assets/110742924/7c3d5621-3e39-4552-9f8d-f28f9668251e)


# Functionality

The Convin REST API follows the following procedure:

## Initiating OAuth Authentication

The endpoint /oauth is responsible for initiating OAuth authentication. It redirects the client to the OAuth server for authentication. The retrieved access token is stored in the session for subsequent requests.

## Retrieving Authorization URL

After initiating OAuth authentication, the endpoint /authorization-url provides the authorization URL. This URL allows the client to authorize the API to access the Google Calendar API using the access token stored in the session.

## Retrieving Events

Once authorized, the endpoint /events can be accessed to retrieve the events from the Google Calendar API. This endpoint uses the access token from the session to fetch the events and returns the event list to the client.

## Help

If you need help you might be able to find an answer on our [docs](https://docs.replit.com) page. Feel free to report bugs and give us feedback [here](https://replit.com/support).
