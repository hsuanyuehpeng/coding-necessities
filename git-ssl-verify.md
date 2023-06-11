To use git with remote repositories with SSL verification enabled, download the CA (.pem/.crt/.cer) from the target server.

For repos on github, that will be github's CA.

After downloading it, open a local repo's

```
.git/config
```

and add the following:
```
[http "https://the.target.server.com/"]
	sslCAinfo = C:/pathToCAFile.crt
```

Then it should be good to go.
