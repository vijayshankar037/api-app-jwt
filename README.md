# What Is Token-based Authentication?
Token-based authentication (also known as JSON Web Token authentication) is a new way of handling the authentication of users in applications. It is an alternative to session-based authentication.

- The most notable difference between the session-based and token-based authentication is that session-based authentication relies heavily on the server. A record is created for each logged-in user.

- Token-based authentication is stateless - it does not store anything on the server but creates a unique encoded token that gets checked every time a request is made.

- Unlike session-based authentication, a token approach would not associate a user with login information but with a unique token that is used to carry client-host transactions. Many applications, including Facebook, Google, and GitHub, use the token-based approach.

# Benefits of Token-based Authentication
- Cross-domain / CORS: Cookies and CORS don't mix well across different domains. A token-based approach allows you to make AJAX calls to any server, on any domain, because you use an HTTP header to transmit the user information.

- Stateless
Tokens are stateless. There is no need to keep a session store since the token is a self-contained entity that stores all the user information in it.

- Decoupling
You are no longer tied to a particular authentication scheme. Tokens may be generated anywhere, so the API can be called from anywhere with a single authenticated command rather than multiple authenticated calls.

- Mobile Ready
Cookies are a problem when it comes to storing user information in native mobile applications. Adopting a token-based approach simplifies this saving process significantly.

- CSRF (Cross Site Request Forgery)
Because the application does not rely on cookies for authentication, it is invulnerable to cross-site request attacks.

- Performance
In terms of server-side load, a network roundtrip (e.g. finding a session on a database) is likely to take more time than calculating an HMACSHA256 code to validate a token and parsing its contents. This makes token-based authentication faster than the traditional alternative.
