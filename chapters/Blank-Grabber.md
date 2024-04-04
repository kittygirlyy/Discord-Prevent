<!-- WARNING HTML -->

<table align="center">
  <tr>
    <th>Title</th>
  </tr>
  <tr>
    <td>BlankGrabber</td>
  </tr>
</table>
<br></br>

<!-- WARNING HTML -->


**Requirements:**

- NodeJS

# Get webhook ?

Hey, if you got Blank-Grabber infection you can delete the webhook easily without deobfuscating python...

---

This grabber use pyinstaller and inject your discord client (PATH: C:\Users\pwnme\AppData\Local\Discord\app-1.0.9012\modules\discord_desktop_core-1\discord_desktop_core), your index.js will be overwrite with malicious code.

## How to delete the webhook if I got injected ?

Copy **index.js** code into a new folder, and `npm init -y` and use this website (https://beautifier.io) to make javascript more readable (Copy beautified javascript into the index.js in your npm project folder)...
Now `npm i electron`, and lets check our obfuscated source code, we just need to search for this `hook = _0x3d8f8e(0x283),` and add this on the next line after `console.log(hook)`.

Let's run this shit in Node runtime with `node index.js` and we got the webhook in base64 LINUX: `echo -n 'EncodedWebhook' | base64 --decode` ; WebBrowser (https://www.base64decode.org)

We got it ! Thanks for reading <3
