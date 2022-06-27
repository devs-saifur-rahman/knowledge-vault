
# OAuth 1.0:

obsolete / discontinued.


# OAuth 2.0


4 character/roles :
* User
* Application
* API/Authoirzation Organization
* Resource Server

## Workflow:

1. Application registers itself in Api/Authorization organization with Name, Website, **Callback URL**.  And it receives a client ID and client secret
2. Authorization: User tries to log in (authorize) to the API server (Authorization Organization) thorugh the Application. Application reaches to API server with its own client ID & secret and asks for certain access permisison. User gets to a screen from the Authorization API server to grant or cancel the access permission. Once user grants the permission, Authorization API server responds to Application with an ID and access token for that user.
3. Authentication: The application then uses those ID and access token to connect and authenticat with the API server (Authorization organization) , and access the Resource Server on behalf of the user.

## Key points 

* OAuth 2.0 is authorization framework
* Authentication happens with [[OpenID Connect ]] with ID and Access Token.


## Grant types :
1. Authorization Grant (Most used - for granting the client app to user's resource)
2. Implicit Grant (superseded by Authorization Grant with PKCE)
3. Password Grant (only for first party app ??)
4. Client Credential Grant ( to update the info of the client app itself)

## Notes:
* "State" - send it along with redirect_url to handle login from different mod of client app. It has secuirty vulnerability - unless encoded with something like JWT. Authorization server will simply return whatever it received .. It has to be maintained by the client app.
* Redirect Url needs to be an exact match i.e - a == b => true but not a?x=1 == b => false.
*  scope values (space-separated)
* avoid using common UUID libraries which often take into account the timestamp or MAC address of the server generating it. A great way to generate a secure secret is to use a cryptographically-secure library to generate a 256-bit value and then convert it to a hexadecimal representation.

## Best Practices
* https://datatracker.ietf.org/doc/html/draft-ietf-oauth-security-topics
* *

# Resources

1. [[https://oauth.net|OAuth.net]]
3. [[https://www.oauth.com/]]
4. [[https://www.youtube.com/watch?v=CPbvxxslDTU|OpenID 2.0 Overview]]
5. [[https://www.youtube.com/watch?v=996OiexHze0|OAuth 2.0 and OpenID Connect]]
6. https://aaronparecki.com/oauth-2-simplified/


## Related topics
1. [[https://indieauth.net|Indie Auth]]  - Client ID / Secret less 
2. [[https://www.w3.org/TR/micropub|MicroPub]]