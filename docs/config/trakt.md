# Trakt Attributes

Configuring [Trakt.tv](https://trakt.tv/) is optional but is required for Trakt based collections to function. 

A `trakt` mapping is in the root of the config file.

Below is a `trakt` mapping example and the full set of attributes:
```yaml
trakt:
  client_id: ################################################################
  client_secret: ################################################################
  pin:
  authorization:
    access_token:
    token_type:
    expires_in:
    refresh_token:
    scope:
    created_at:
```

| Attribute       | Allowed Values                  | Default | Required |
|:----------------|:--------------------------------|:-------:|:--------:|
| `client_id`     | Trakt Application Client ID     |   N/A   | &#9989;  |
| `client_secret` | Trakt Application Client Secret |   N/A   | &#9989;  |
| `pin`           | Trakt Pin                       |  None   | &#10060; |

* All other attributes will be filled in by the script. 

* To connect to Trakt.tv you must create a Trakt application and supply the script the `client_id`, `client_secret`, and `pin` provided, please do the following:
1. [Click here to create a Trakt API application.](https://trakt.tv/oauth/applications/new)
2. Enter a `Name` for the application.
3. Enter `urn:ietf:wg:oauth:2.0:oob` for `Redirect uri`.
4. Click the `SAVE APP` button.
5. Record the `Client ID` and `Client Secret` as `client_id` and `client_secret` in your Configuration File.
6. Click the Green Authorize Button next to the Redirect URI

    ![Trakt Authorize](trakt.png)
8. Record the `PIN` as `pin` in your Configuration File.

* Run the script shortly after obtaining your PIN; the PIN may expire at some point.
