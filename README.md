# testcafe-repro-old-headless-chromium

## Fetch An Old Version of Chrome

You need an old version of Chrome.
The simplest solution is to use a portable app.

All portable versions of Google Chrome: <https://sourceforge.net/projects/portableapps/files/Google%20Chrome%20Portable/>

1. downloa i.e. <https://sourceforge.net/projects/portableapps/files/Google%20Chrome%20Portable/GoogleChromePortable_88.0.4324.190_online.paf.exe/download>
2. store in the root of this repository
3. execute/"install"

## Run Tests

* "normal": `npx testcafe chromium:.\GoogleChromePortable\GoogleChromePortable.exe .\test.tc.js`
* headless: `npx testcafe chromium:.\GoogleChromePortable\GoogleChromePortable.exe:headless .\test.tc.js`