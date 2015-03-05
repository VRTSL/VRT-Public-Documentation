Name2Key API
============

Better Name2Key Documentation will end up here at some point!

Basically, pass an avatars username to [https://name2key.azurewebsites.net/Name2Key/](https://name2key.azurewebsites.net/Name2Key/)



And its key returns in either JSON or XML, a null key returns if agent is not found.

This should work with all maturity settings on profiles

in lsl a function for this would look something like:
```c-like

key Name2KeyRequest( string inName ) {
    return llHTTPRequest( "https://name2key.azurewebsites.net/Name2Key/" + llEscapeURL(inName), [HTTP_METHOD, "GET", HTTP_MIMETYPE, "application/json"], "" );
}

`