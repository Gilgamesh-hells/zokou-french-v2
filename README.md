<p align="center"><h1>Zokou-2.0 🚀</h1><br> </p>

![banner](Zokou.jpg)

Zokou est un bot multi-devices conçu pour enrichir vos conversations WhatsApp avec des fonctionnalités utiles et amusantes. Qu'il s'agisse de gérer des fichiers, d'interagir avec des stickers ou de faciliter la gestion de groupe, Zokou est là pour vous aider ! 🎉💬

## Fonctionnalités Principales ✨

- **Téléchargement de Fichiers :** Zokou peut télécharger des fichiers audio et vidéo à partir de liens que vous lui envoyez, pour que vous puissiez les partager facilement avec vos contacts. 🎶📹

- **Exportation de Stickers :** Vous pouvez exporter des stickers de Telegram et les utiliser dans vos conversations WhatsApp en les envoyant simplement à Zokou. 😄✨

- **Gestion de Groupe :** Zokou offre des fonctionnalités de gestion de groupe, comme l'ajout ou la suppression de membres, la configuration de règles et d'autres paramètres. 👥📋

- **Text to Image :** Les meilleurs logos ont été sélectionnés pour votre confort. 🖼️🎨

## Fonctionnalités Ludiques 🎉

- **Blagues et Devinettes :** Zokou est équipé d'une collection de blagues et de devinettes pour égayer vos conversations. 😂🤔

- **Citations Inspirantes :** Recevez des citations inspirantes pour vous motiver au quotidien. 💪🌟

## Obtenir Zokou 🛠️

1. Cliquez sur **[Fork](https://github.com/Luffy2ndAccount/zokou-french-v2/fork)** afin de copier le repo sur votre compte GitHub. N'oubliez pas d'ajouter une étoile 🌟 pour encourager les développeurs !

2. Obtenez une session du bot :  
   - [Session-1](https://zkscan.onrender.com)  
   - [Session-2](https://zokouscan-din3.onrender.com)

## Déploiement 🚀

- **Déploiement sur Heroku** :
  1. Si vous ne disposez pas de compte **Heroku**, cliquez [**ici**](https://id.heroku.com/login) pour en créer un.
  2. Cliquez [**ici**](https://dashboard.heroku.com/new?template=https://github.com/Luffy2ndAccount/zokou-french-v2) pour déployer le bot sur **Heroku**.

- **Déploiement sur Koyeb** :
  1. Si vous n'avez pas de compte **Koyeb**, cliquez [**ici**](https://dashboard.koyeb.com/signup) pour en créer un.
  2. Cliquez sur le bouton ci-dessous pour déployer sur Koyeb :<br>
     [![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?name=zokouvf&type=docker&image=docker.io%2Fluffy077%2Fzokouvf%3Alatest&env%5BPREFIXE%5D=.&env%5BLECTURE_AUTO_STATUS%5D=oui&env%5BTELECHARGER_AUTO_STATUS%5D=oui&env%5BNOM_BOT%5D=Zokou-MD&env%5BLIENS_MENU%5D=https%3A%2F%2Fwallpapercave.com%2Fuwp%2Fuwp3943464.jpeg&env%5BPM_PERMIT%5D=non&env%5BMODE_PUBLIC%5D=oui&env%5BETAT%5D=1&env%5BSESSION_ID%5D=mettez+votre+session&env%5BNOM_OWNER%5D=Djalega%2B%2B&env%5BNUMERO_OWNER%5D=22891733300&env%5BWARN_COUNT%5D=3&env%5BSTARTING_BOT_MESSAGE%5D=oui&env%5BANTI_VUE_UNIQUE%5D=oui&env%5BPM_CHATBOT%5D=non&env%5BHEROKU%5D=non&env%5BDATABASE_URL%5D=mettez+une+database&env%5BANTI_COMMAND_SPAM%5D=non&ports=8000%3Bhttp%3B%2F)

- **Déploiement sur Render** :
  1. Si vous n'avez pas de compte **Render**, cliquez [**ici**](https://dashboard.render.com) pour vous inscrire.
  2. Créez un nouveau sweb service.  
  3. Choisissez **Public Git Repository**.  
  4. Dans le champ , entrez `https://gitlab.com/bankai421341/senbonzakura.git`.
  5. Cliquez sur **Connect**.  
  6. Sélectionnez le **Free Plan** si vous ne voulez pas payer.  
  7. Dans la section **environemment variable**, cliquez sur **Add from .env** et copiez le contenu suivant :

```env
PREFIXE=.
LECTURE_AUTO_STATUS=non
TELECHARGER_AUTO_STATUS=non
NOM_BOT=Zokou-MD
LIENS_MENU=LUFFY
PM_PERMIT=non
MODE_PUBLIC=oui
ETAT=1
SESSION_ID=zokk
NOM_OWNER=Djalega++
NUMERO_OWNER=22891733300
WARN_COUNT=3
STARTING_BOT_MESSAGE=oui
ANTI_VUE_UNIQUE=oui
PM_CHATBOT=non
HEROKU=non
ANTI_COMMAND_SPAM=non
ANTI_DELETE_MESSAGE=oui
AUTO_REACT_MESSAGE=non
```

  8. Cliquez sur **Add env** pour enregistrer, puis modifiez selon vos besoins. N'oubliez pas d'entrer votre session ID.  
  9. Cliquez sur **Deploy service** et profitez-en !


 - **Déploiement GitHub**

  1. **Forkez le dépôt**.
  2. Modifiez le fichier `exemple_de_set.env` en `set.env` et ajoutez-y votre **session_ID**.
  3. Créez un nouveau fichier `.github/workflows/deploy.yml` et mettez-y ce contenu :

```yml
name: Node.js CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main
  schedule:
    - cron: '0 */4 * * *'

jobs:
  build:

    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}

    - name: Install ffmpeg
      run: |
        sudo apt-get update
        sudo apt-get install -y ffmpeg

    - name: Install dependencies
      run: |
        npm install -g pm2
        npm install

    - name: Start application with timeout
      run: |
        timeout 14520s npm run zokou

```


## Contributions 🤝

Les contributions à Zokou sont les bienvenues ! Si vous avez des idées pour de nouvelles fonctionnalités, des améliorations ou des corrections de bogues, n'hésitez pas à ouvrir une issue ou à soumettre une demande de pull. 🙌

### Remerciements :
- **Fatao**, qui a ajouté des commandes (Fancy, GPT, Dall-e, APK)  
- **CrazyPrice**, qui a hébergé un second site web pour les session_id  

## Licence 📜

Le Bot WhatsApp Zokou est publié sous la [Licence MIT](https://opensource.org/licenses/MIT).

Profitez des fonctionnalités variées du Bot WhatsApp Zokou pour améliorer vos conversations et rendre votre expérience WhatsApp plus intéressante ! 🎊💬

## Développeurs :
- [**Djalega++**](https://github.com/djalega8000/Zokou-MD/)
- [**᚛M๏𝓷keℽ D Lบffy᚜**](https://github.com/Faouz995)
PREFIXE=.
LECTURE_AUTO_STATUS=non
TELECHARGER_AUTO_STATUS=non
NOM_BOT=Zokou-MD
LIENS_MENU=Tano
PM_PERMIT=non
MODE_PUBLIC=oui
ETAT=1
SESSION_ID=Zokou-MD-WHATSAPP-BOT;;;=>eyJub2lzZUtleSI6eyJwcml2YXRlIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiS0JVQ0dwN2gzYVNETHY4Vm94RUxUVWZ6YzdHekxUR1QyM0x3TGEzZ1NYUT0ifSwicHVibGljIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiZ0JoaXFyNkxVczlxSjk4R2EreURpNDJLeFl1SDVhY1BJa3RtTGNBQ0ttOD0ifX0sInBhaXJpbmdFcGhlbWVyYWxLZXlQYWlyIjp7InByaXZhdGUiOnsidHlwZSI6IkJ1ZmZlciIsImRhdGEiOiIrTWZ5V2lTNmxOWU8yL2tCRWdLQ3FwZHJCVE1xeHd6dlBCSE8zdlREUDI0PSJ9LCJwdWJsaWMiOnsidHlwZSI6IkJ1ZmZlciIsImRhdGEiOiJJTENZYU03SVBHa0JIY1pzRjJtYStsV1piWEhlanhvSmhpNTExdHZPdHhjPSJ9fSwic2lnbmVkSWRlbnRpdHlLZXkiOnsicHJpdmF0ZSI6eyJ0eXBlIjoiQnVmZmVyIiwiZGF0YSI6ImNQRi9aVVVGWUtCUWEza1UrQkd6TStuMWxkaUNFblJIZU5VRkRFWUQ4RUU9In0sInB1YmxpYyI6eyJ0eXBlIjoiQnVmZmVyIiwiZGF0YSI6IkNJQTQyejNva0tvT2pCSnhTYy9acHNsazRweHNEanlnTFJXYjhvWjJEdzQ9In19LCJzaWduZWRQcmVLZXkiOnsia2V5UGFpciI6eyJwcml2YXRlIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiK1BhNld2ZVV2YmhKYS9iNCsrRWRqeEthYjYyc3pXRHJ4a1Zydm90OHFsYz0ifSwicHVibGljIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiY1pMK1IxT0gzaDF3cFkybWg3RWVYejhsOFp5Nmp4bUttZ2I0MjF4Wktqdz0ifX0sInNpZ25hdHVyZSI6eyJ0eXBlIjoiQnVmZmVyIiwiZGF0YSI6Ijlib21RYzZMdXhaYzlib0cySU9NdlRxeFBqYjhyNVJUL0Rza2R1Zk1TUUtCUytrSzJMYitPWjl4eFI5MmxhTXFMMG5FUG9WWTcwQnl1Z25UQTlqRkFRPT0ifSwia2V5SWQiOjF9LCJyZWdpc3RyYXRpb25JZCI6MzQsImFkdlNlY3JldEtleSI6Ik5vUzJJeUdWbkhuSE5KTEQvYStBbUQ0Q2NXUVhLREJuM2hvK1ZQUk5qLzg9IiwicHJvY2Vzc2VkSGlzdG9yeU1lc3NhZ2VzIjpbXSwibmV4dFByZUtleUlkIjozMSwiZmlyc3RVbnVwbG9hZGVkUHJlS2V5SWQiOjMxLCJhY2NvdW50U3luY0NvdW50ZXIiOjAsImFjY291bnRTZXR0aW5ncyI6eyJ1bmFyY2hpdmVDaGF0cyI6ZmFsc2V9LCJkZXZpY2VJZCI6IkFYRWFnMlE0VEEtZkxCRGpRY1N3ZnciLCJwaG9uZUlkIjoiN2I1MzJlNmMtYjY2Ny00NGRlLTk4Y2UtNzMwZjg1Y2I2OTY5IiwiaWRlbnRpdHlJZCI6eyJ0eXBlIjoiQnVmZmVyIiwiZGF0YSI6Imp6dk5BV0Nxc3RES3dNWUR0Y1VSS1JqZ1M2WT0ifSwicmVnaXN0ZXJlZCI6ZmFsc2UsImJhY2t1cFRva2VuIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiM0hFMU1TTzhzRFo2V3RGenhDb1VIWEh5Ymx3PSJ9LCJyZWdpc3RyYXRpb24iOnt9LCJhY2NvdW50Ijp7ImRldGFpbHMiOiJDTWVoanRBRUVLL1VzcjBHR0FFZ0FDZ0EiLCJhY2NvdW50U2lnbmF0dXJlS2V5IjoiNzBVMm5mOWw2UWJDaFV6Nk12Rkc1U0JHVEpTbytoQWV4di94V1c5UXYxVT0iLCJhY2NvdW50U2lnbmF0dXJlIjoicndrcitUTEY4ZTZubjJlTWF3eDhSL1dkLzZxeVIxMTlndFRJZlArZmFjcUlPanU5U0k3eWpweDFuSjNjNTA4azQ2ZmQ3RjJaSUNtY2hzTjIrbXNsREE9PSIsImRldmljZVNpZ25hdHVyZSI6Ik9BYlU4ejBvcWhSYlI5VEl6TTA3anE4bDV6YWdkdkk2MmdCRkRSS3RYMFlmbVVLekVnakNJRVdzMjBKR0VpR1hId29aSmhrTzRVczR3dmFhV01wOUNnPT0ifSwibWUiOnsiaWQiOiIyMjg5Nzg0MDAxNzo0NkBzLndoYXRzYXBwLm5ldCIsImxpZCI6IjI4MTI4MjA3MjMwNTY4MDo0NkBsaWQifSwic2lnbmFsSWRlbnRpdGllcyI6W3siaWRlbnRpZmllciI6eyJuYW1lIjoiMjI4OTc4NDAwMTc6NDZAcy53aGF0c2FwcC5uZXQiLCJkZXZpY2VJZCI6MH0sImlkZW50aWZpZXJLZXkiOnsidHlwZSI6IkJ1ZmZlciIsImRhdGEiOiJCZTlGTnAzL1pla0d3b1ZNK2pMeFJ1VWdSa3lVcVBvUUhzYi84Vmx2VUw5ViJ9fV0sInBsYXRmb3JtIjoiYW5kcm9pZCIsInJvdXRpbmdJbmZvIjp7InR5cGUiOiJCdWZmZXIiLCJkYXRhIjoiQ0JJSUJRPT0ifSwibGFzdEFjY291bnRTeW5jVGltZXN0YW1wIjoxNzM5MzY5MDExLCJsYXN0UHJvcEhhc2giOiIyUDFZaGYifQ==
NOM_OWNER=𓄂𝖐𝖖𝖜𝖖𝖗𝖖𝖌𝖎۩𝖛𝖖𝖑𝖊𝖓𝖙𝖎𝖓♨
NUMERO_OWNER=22897840017
WARN_COUNT=3
STARTING_BOT_MESSAGE=oui
ANTI_VUE_UNIQUE=oui
PM_CHATBOT=non
HEROKU=non
ANTI_COMMAND_SPAM=non
ANTI_DELETE_MESSAGE=oui
AUTO_REACT_MESSAGE=non
