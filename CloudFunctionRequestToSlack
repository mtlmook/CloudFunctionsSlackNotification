def hello_world(request):
    import requests 
    from requests.structures import CaseInsensitiveDict
    """Responds to any HTTP request.
    Args:
        request (flask.Request): HTTP request object.
    Returns:
        The response text or any set of values that can be turned into a
        Response object using
        `make_response <http://flask.pocoo.org/docs/1.0/api/#flask.Flask.make_response>`.
    """
    print("Github Webhook received")
    url="https://hooks.slack.com/services/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"
    headers=CaseInsensitiveDict()
    headers["Content-Type"]="application/json"

    data='{"text":"Github Activity - Push, Pull or any other event"}'
    resp=requests.post(url,headers=headers,data=data)
    print(resp.status_code)
    return resp.status_code
