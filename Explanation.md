1. What was the bug?

When the OAuth2 token was provided as a dictionary, the client did not refresh it even if it was expired.

2. Why did it happen?

The refresh logic only checked expiration when the token was an instance of OAuth2Token. Dictionary tokens bypassed expiration checking.

3. Why does your fix solve it?

The updated condition ensures that any token that is not an OAuth2Token instance triggers a refresh, guaranteeing a valid token before API requests.

4. One realistic edge case not covered

The tests do not verify behavior when a dictionary token contains malformed or missing fields.