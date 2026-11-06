# Guardián 2FA Privacy Policy

[English](#english) · [Español](#español)

Last updated: November 5, 2026

## English

Guardián 2FA is a browser extension that generates two-factor authentication (2FA) codes. It is published by Morales Devop. The developer runs no servers for this extension and does not receive, store, or have access to your data.

### What the extension handles

| Data | Where it goes | Purpose |
|---|---|---|
| 2FA accounts (secret keys, issuer, account labels) and settings | Your browser's local extension storage. Encrypted if you set a vault password; otherwise stored unencrypted on your device. | Generating your codes |
| Encrypted backup of your accounts (only if you turn on Google sync) | A private app folder in your own Google Drive | Backing up and syncing your codes |
| Google account email address (only if you sign in with Google) | Requested from Google and shown in the extension while the panel is open. It is not saved. | Showing which account is signed in |
| Google account identifier (only if you turn on Google sync) | A numeric identifier from Google, kept in your local vault | Making sure your backup only goes to the account you chose |
| Codes removed by a sync (only if a sync removes codes from this device) | Kept in your local vault for up to 30 days, or until you restore them | Letting you get them back |
| Google access token (only if you sign in with Google) | Your browser's session storage, which is cleared when the browser closes | Accessing the app folder in your Drive |
| Encrypted copy of your accounts (only if you turn on Browser Sync) | Your browser's sync service | Syncing between your browsers |
| Address and title of the active tab | Used inside the extension only. Never stored or sent anywhere. | Suggesting the code for the site you are on |
| Screen capture of the active tab (only when you start a page QR scan) | Processed on your device and not stored or sent anywhere | Reading a QR code you selected |

The extension does not use analytics, advertising, or tracking. It does not sell your data or share it with anyone. Its only network requests go to Google, and only if you sign in with Google.

### Google sync

Google sync is optional. When you turn it on:

- Google's own sign-in window handles your login. The extension never sees your Google password.
- Your codes are encrypted on your device with a backup password you choose (AES-256-GCM with a key derived using PBKDF2) before they are uploaded. Google receives only the encrypted data.
- The extension requests two permissions: `drive.appdata`, for its own private app folder, and `userinfo.email`, for your email address. It cannot see any of your other Google Drive files.
- Your backup password is not stored. A key derived from it is kept in your local vault so that sync can run. If you did not set a vault password, this key is stored unencrypted on your device, like your codes. If you forget the backup password, nobody can recover the backup.
- Google can see the backup file's name, size, and dates, and the encryption settings stored with it, but not your codes.

Guardián 2FA's use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements. Google handles your account under the [Google Privacy Policy](https://policies.google.com/privacy).

### Browser permissions

- **storage:** saves your accounts and settings.
- **activeTab and scripting:** when you use the extension on a page, read its address and title to suggest a code, scan a QR code, or paste a code.
- **sidePanel** (Chrome and Edge): opens the extension in the side panel.
- **identity:** opens Google's sign-in window.

### Your choices and deleting your data

- **Turn off sync or sign out:** use **Settings → Google backup**. Signing out revokes the extension's current access token, if one is active. Your codes stay on your device and your backup stays in Drive until you delete them.
- **Delete the backup from Google Drive:** use **Settings → Google backup → Delete Google backup**. You can also open Google Drive → **Settings → Manage apps**, find Guardián 2FA, and choose **Delete hidden app data**. If sync is still on in another device, that device uploads its copy again, so turn it off there first.
- **Delete codes kept after a sync:** use **Discard these codes** in the same panel. Otherwise they are removed after 30 days.
- **Remove the extension's access to your Google account:** go to [your Google account's third-party connections](https://myaccount.google.com/connections).
- **Delete local data:** uninstalling the extension removes its local storage.

Because the developer holds none of your data, the developer cannot access, restore, or delete it for you. You are responsible for keeping your own backups and recovery methods.

### Children

Guardián 2FA is not directed at children and does not knowingly collect their information.

### Changes and contact

If this policy changes, the new version will be published at this address with a new date. For questions, write to alexpc778@gmail.com.

## Español

Guardián 2FA es una extensión de navegador que genera códigos de verificación en dos pasos (2FA). La publica Morales Devop. El desarrollador no opera servidores para esta extensión y no recibe, guarda ni puede ver tus datos.

### Qué datos maneja la extensión

| Dato | Dónde queda | Para qué |
|---|---|---|
| Cuentas 2FA (claves secretas, emisor, nombres de cuenta) y ajustes | Almacenamiento local de la extensión en tu navegador. Se cifran si pones una contraseña al vault; si no, quedan sin cifrar en tu dispositivo. | Generar tus códigos |
| Copia cifrada de tus cuentas (solo si activas la sincronización con Google) | Una carpeta privada de la app en tu propio Google Drive | Respaldar y sincronizar tus códigos |
| Correo de tu cuenta de Google (solo si inicias sesión con Google) | Se pide a Google y se muestra en la extensión mientras el panel está abierto. No se guarda. | Mostrar con qué cuenta iniciaste sesión |
| Identificador de tu cuenta de Google (solo si activas la sincronización con Google) | Un identificador numérico de Google, guardado en tu vault local | Asegurar que tu copia solo vaya a la cuenta que elegiste |
| Códigos quitados por una sincronización (solo si una sincronización quita códigos de este dispositivo) | Se guardan en tu vault local hasta 30 días, o hasta que los recuperes | Permitirte recuperarlos |
| Token de acceso de Google (solo si inicias sesión con Google) | Almacenamiento de sesión del navegador, que se borra al cerrarlo | Acceder a la carpeta de la app en tu Drive |
| Copia cifrada de tus cuentas (solo si activas Browser Sync) | El servicio de sincronización de tu navegador | Sincronizar entre tus navegadores |
| Dirección y título de la pestaña activa | Se usan solo dentro de la extensión. No se guardan ni se envían a ningún sitio. | Sugerir el código de la página en la que estás |
| Captura de la pestaña activa (solo al iniciar un escaneo de QR en la página) | Se procesa en tu dispositivo y no se guarda ni se envía a ningún sitio | Leer el código QR que seleccionaste |

La extensión no usa analítica, publicidad ni rastreo. No vende tus datos ni los comparte con nadie. Sus únicas peticiones de red van a Google, y solo si inicias sesión con Google.

### Sincronización con Google

La sincronización con Google es opcional. Cuando la activas:

- El inicio de sesión ocurre en la ventana oficial de Google. La extensión nunca ve tu contraseña de Google.
- Tus códigos se cifran en tu dispositivo con una contraseña de copia que eliges tú (AES-256-GCM, con clave derivada mediante PBKDF2) antes de subirse. Google solo recibe los datos cifrados.
- La extensión pide dos permisos: `drive.appdata`, para su propia carpeta privada, y `userinfo.email`, para tu correo. No puede ver ningún otro archivo de tu Google Drive.
- Tu contraseña de copia no se guarda. En tu vault local se guarda una clave derivada de ella para que la sincronización funcione. Si no pusiste contraseña al vault, esta clave queda sin cifrar en tu dispositivo, igual que tus códigos. Si olvidas la contraseña de copia, nadie puede recuperar la copia.
- Google puede ver el nombre, el tamaño y las fechas del archivo de copia, y los ajustes de cifrado guardados con él, pero no tus códigos.

El uso y la transferencia de la información recibida de las API de Google por parte de Guardián 2FA cumplen la [Política de datos de usuario de los servicios de API de Google](https://developers.google.com/terms/api-services-user-data-policy), incluidos los requisitos de uso limitado. Google trata tu cuenta según la [Política de privacidad de Google](https://policies.google.com/privacy).

### Permisos del navegador

- **storage:** guarda tus cuentas y ajustes.
- **activeTab y scripting:** cuando usas la extensión en una página, leen su dirección y título para sugerir un código, escanear un QR o pegar un código.
- **sidePanel** (Chrome y Edge): abre la extensión en el panel lateral.
- **identity:** abre la ventana de inicio de sesión de Google.

### Tus opciones y cómo borrar tus datos

- **Desactivar la sincronización o cerrar sesión:** ve a **Ajustes → Copia en Google**. Al cerrar sesión se revoca el token de acceso actual de la extensión, si hay uno activo. Tus códigos siguen en tu dispositivo y tu copia sigue en Drive hasta que los borres.
- **Borrar la copia de Google Drive:** ve a **Ajustes → Copia en Google → Borrar copia de Google**. También puedes abrir Google Drive → **Configuración → Administrar aplicaciones**, buscar Guardián 2FA y elegir **Eliminar datos ocultos de la aplicación**. Si otro dispositivo sigue con la sincronización activa, volverá a subir su copia, así que desactívala antes allí.
- **Eliminar los códigos guardados tras una sincronización:** usa **Descartar estos códigos** en el mismo panel. Si no, se eliminan a los 30 días.
- **Quitar el acceso de la extensión a tu cuenta de Google:** ve a [las conexiones con terceros de tu cuenta de Google](https://myaccount.google.com/connections).
- **Borrar los datos locales:** al desinstalar la extensión se borra su almacenamiento local.

Como el desarrollador no tiene ninguno de tus datos, no puede verlos, restaurarlos ni borrarlos por ti. Eres responsable de mantener tus propias copias y métodos de recuperación.

### Menores

Guardián 2FA no está dirigida a menores y no recopila su información a sabiendas.

### Cambios y contacto

Si esta política cambia, la nueva versión se publicará en esta dirección con una fecha nueva. Si tienes preguntas, escribe a alexpc778@gmail.com.
