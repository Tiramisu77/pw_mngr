### pw_mngr

A tiny, portable password manager, built around `localStorage` and `window.crypto` APIs. Data is encrypted with AES-GCM, key is derived with PBKDF2, random passwords are generated with `crypto.getRandomBytes` and presented in base64 form.

### demo page

https://tiramisu77.github.io/pw_mngr/

#### console commands

`pw_mngr.exportEncryptedStorage()` - outputs encrypted and base64-encoded password storage, in format: `salt;iv;ciphertext`

`pw_mngr.importEncryptedStorage(newStorage: string)` - replaces the current encrypted storage with a new one (old storage will be discarded)

`pw_mngr.exportPlaintextStorage()` - outputs json string representing the current password storage

`pw_mngr.importPlaintextStorage(newStorage: string, merge=false)` - parses newStorage as json, if merge set to true, adds all entries to the current storage, otherwise replaces current storage with a new one
