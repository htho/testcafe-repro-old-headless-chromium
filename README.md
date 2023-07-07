# testcafe-repro-old-headless-chromium

## Fetch An Old Version of Chrome

You need an old version of Chrome.
The simplest solution is to use a portable app.

All portable versions of Google Chrome: <https://sourceforge.net/projects/portableapps/files/Google%20Chrome%20Portable/>

1. download the portable browsers to `./`
   * the last version that does not work (Chrome 94): <https://sourceforge.net/projects/portableapps/files/Google%20Chrome%20Portable/GoogleChromePortable_94.0.4606.81_online.paf.exe/download>
   * the first version that does work (Chrome 95): <https://sourceforge.net/projects/portableapps/files/Google%20Chrome%20Portable/GoogleChromePortable_95.0.4638.69_online.paf.exe/download>
2. execute the installer and store in `./GoogleChromePortable94/` and `./GoogleChromePortable95/`

## Run Tests

* Chrome 95 works as expected
  * "normal": `npx testcafe chromium:.\GoogleChromePortable95\GoogleChromePortable.exe .\test.tc.js`
  * headless: `npx testcafe chromium:.\GoogleChromePortable95\GoogleChromePortable.exe:headless .\test.tc.js`
* Chrome 94 does not work
  * "normal" - trows `TypeError`: `npx testcafe chromium:.\GoogleChromePortable94\GoogleChromePortable.exe .\test.tc.js`
  * headless - does nothing ("hangs"): `npx testcafe chromium:.\GoogleChromePortable94\GoogleChromePortable.exe:headless .\test.tc.js`