Example:
```yaml
...
headers:
  Rate-Limit-Limit:
    description: The number of allowed requests in the current period
    type: integer
...
paths:
  /api-keys:
    get:
      summary: Retrieve a list of api keys
      responses:
        200:
          description: A list of api keys was retrieved successfully
          headers:
            Rate-Limit-Limit:
              $ref: "#/headers/Rate-Limit-Limit"
```