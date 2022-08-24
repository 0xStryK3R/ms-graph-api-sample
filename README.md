## Setup

1. Setup Virtual Environment with bellow command:
    ```console
    python -m venv .venv
    ```

2. Activate Virtual Environment (Windows Only):
    ```console
    .venv\Scripts\activate
    ```

3. Install below modules:
    ```console
    python3 -m pip install azure-identity
    python3 -m pip install msgraph-core
    ```

## Run

1. Update below details in `config.cfg`:
    ```config
    [azure]
    clientId = YOUR_CLIENT_ID_HERE
    clientSecret = YOUR_CLIENT_SECRET_HERE_IF_USING_APP_ONLY
    tenantId = YOUR_TENANT_ID_HERE_IF_USING_APP_ONLY
    authTenant = common
    graphUserScopes = User.Read Mail.Read Mail.Send
    user_smtp = 
    user_id =
    ``` 
    > For App-Only, update ***`clientId`, `clientSecret`, `tenantId`*** and ***`user_smtp`*** or ***`user_id`***

2. Run `main.py` file in activated virtual environment with below command:
    ```console
    python main.py
    ```

## References
- [Sample Reference](https://docs.microsoft.com/en-us/graph/tutorials/python?tabs=aad)

- [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer)

- [Documentation](https://docs.microsoft.com/en-us/graph/api/overview?view=graph-rest-1.0)