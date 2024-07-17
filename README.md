# nao deu certo fazer o deploy pelo fleek , apartir de um template react
`💡 Please follow the setup instructions to create a valid configuration file.

✔ We've found existing sites. Would you like to link to one of them? … yes
</br>
✔ Select site from the list › exerciseZEROfleek</br>
✔ Please specify the directory containing the site files to be uploaded … .</br>
✔ Would you like to include the optional "build" command? … no</br>
✔ Select a format for saving the site's configuration: › JSON (fleek.config.json)</br>
Warning: The `ipfs` service in Fleek SDK will be deprecated. Please use `storage` service instead</br>
✅ Success! Deployed!</br>
</br>
> Site IPFS Content Identifier (CID): QmV4eyichqU7LCF7ZPWLnrDurqpnvGN5GCGqEoYdaVYRmN</br>
💡 You can access it through the gateway:`</br>
🔗 https://wide-fountain-small.on-fleek.app

# modivo do erro 
|
eu estava fazendo um deploy no do site fleek , e n deu certo ...</br>
apareceu este erro "Warning: The `ipfs` service in Fleek SDK will be deprecated.</br>
Please use `storage` service instead</br>
❌ Error: Upload failed."   </br>
segui todos os passos e depois de executar o comando no terminal "fleek sites deploy"</br>   
ele apareceu a mensagem de erro que te enviei .</br> 
Para vc ia me ajudar a proceder com o meu deploy .</br> 
E para vc fazer mais rapido deixo aqui o link da documentação do site fleek aap.fleek.xzy (https://fleek.xyz/docs/cli/)</br>
</br>
Entendi, parece que o problema está relacionado à depreciação do serviço ipfs no SDK do Fleek. Aqui estão alguns passos que você pode seguir para resolver o problema:
</br>
Atualize o SDK do Fleek: Certifique-se de que você está usando a versão mais recente do SDK do Fleek.</br>
Isso pode resolver problemas de compatibilidade.</br>
Use o serviço storage: Como a mensagem de erro sugere, você deve usar o serviço storage em vez do ipfs.</br>
Verifique a documentação para ver como fazer essa mudança.[from docs link](https://fleek.xyz/docs/cli/storage/) </br> 
Verifique a configuração do seu projeto: Certifique-se de que todas as configurações no seu arquivo `.fleek.json` estão corretas e atualizadas.</br>
Aqui está um exemplo de como pode ser configurado:</br>
JSON</br>
</br>
</br>
```
{
  "build": {
    "image": "node:alpine",
    "command": "npm install && npm run build",
    "publicDir": "build",
    "environment": {
      "NODE_ENV": "production"
    }
  }
}
```
Reinicie o deploy: Após fazer as alterações necessárias, tente reiniciar o deploy com o comando:
fleek sites deploy
</br>
Se o problema persistir, você pode consultar a documentação do Fleek para mais detalhes ou abrir um ticket de suporte no site do Fleek12.</br>
1: Fleek Documentation - Site Deployment 2: Fleek Support - Deploy fails with no error message</br>
Saiba mais 1docs.fleek.co______2support.fleek.xyz______3docs.fleek.co___4docs.fleek.co____5github.com</br>

# React Boilerplate
![React Boilerplate](https://github.com/fleek-tools/react-template/assets/74613246/443647a2-26bd-4872-aafd-fe6a16f0e2f5)


## 🚀 Project Structure



Inside of your React project, you'll see the following folders and files:

```
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/
│   ├── main.tsx
│   ├── App.tsx
│   └── App.css
├── index.html
├── tsconfig.json
├── vide.config.ts
└── package.json
```

If you want to learn more about `vite` and `react` you can checkout [Vite Documentation](https://vitejs.dev/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `pnpm install`          | Installs dependencies                            |
| `pnpm run dev`          | Starts local dev server at `localhost:3000`      |
| `pnpm run build`        | Build your production site to `./dist/`          |
| `pnpm run preview`      | Preview your build locally, before deploying     |
| `pnpm run lint ...`    | Run Linter |

## ⚡ How to deploy to Fleek

# [link from docs to deploy](https://fleek.xyz/docs/cli/)

### 1. Create a `fleek.json` config file:


#### You need to have Nodejs >= 18.18.2
`npm install -g @fleek-platform/cli
`
#### To confirm if it was installed , execute this on terminal
`fleek version
`
#### Get all the available command list by running:
`fleek
`
#### Cria o init, para logar pelo link
`fleek sites init`


You can configure this site deployment using [Fleek CLI]() and running:
```
 > fleek sites init
   WARN! Fleek CLI is in beta phase, use it under your own responsibility
   ? Choose one of the existing sites or create a new one. › 
   ❯ Create a new site
```
It will prompt you for a `name`, `dist` directory location & `build command`
- `name`: How you want to name the site
- `dist`: The output directory where the site is located, for this template it's `dist`
- `build command`: Command to build your site, this will be used to deploy the latest version either by CLI or Github Actions


# colar aqui o print do confirm na plataforma fleek

#### Seleciona um projeto exibido pelo terminal, clicando enter

# ou se caso quiser associar novos arquivos à um site ja existente vai aparecer esta sms e vc digita Y
` We've found existing sites. Would you like to link to one of them? … yes`
*em seguida escolher qual site dos que ja tem*
preciona enter se so tiver um
`Select site from the list › exerciseZEROfleek`



#### Agora nome do site 
escolhi `exerciseZEROfleek` pois n alterei algo

#### informar o local do diretorio que tem o código fonte de site
coloque um ponto no terminal    .
`Please specify the directory containing the site files to be uploaded > .
`

#### colocar comandos builds opcionais
coloquei no terminal `y`

##### se for escolhido colocar bilds deu um erro e escolha n colocar builds

#### escolher formatos de consiguração (typescript, javascript, JSON) 
colocar aqui a imagem que tirei print 
escolhi json `Select a format for saving the site's configuration: › JSON (fleek.config.json)`


### 2. Deploy the site
After configuiring your `fleek.json` file, you can deployt the site by running
./
```
fleek sites deploy
```

#### Para mim deu erro

`Warning: The `ipfs` service in Fleek SDK will be deprecated. Please use `storage` service instead
❌ Error: Upload failed.`

# problema está relacionado à depreciação do serviço ipfs no SDK do Fleek

After running it you will get an output like this:
```
 WARN! Fleek CLI is in beta, use it at your own discretion
 > Success! Deployed!
 > Site IPFS CID: QmP1nDyoHqSrRabwUSrxRV3DJqiKH7b9t1tpLcr1NTkm1M

 > You can visit through the gateway:
 > https://ipfs.io/ipfs/QmP1nDyoHqSrRabwUSrxRV3DJqiKH7b9t1tpLcr1NTkm1M
 ```

### Extra features
- **Continuous Integration (CI):** `fleek sites ci` [Documentation.](https://docs.fleek.xyz/services/sites/#continuous-integration-ci)
- **Adding custom domains:** `fleek domains create` [Documentation.](https://docs.fleek.xyz/services/domains/)


### Keep in mind:

This template has been configured to produce a static output.

```js
// vite.config.ts

import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react-swc'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  base: "./",
})
```

This means that assets will be pre-fixed with `./`, you can learn more about it in [Vite Documentation](https://vitejs.dev/config/shared-options.html#base)


## 👀 Want to learn more?

Feel free to check [React documentation](https://react.dev/) or [Vite Documentation](https://vitejs.dev/guide/).

