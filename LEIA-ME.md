# Giro Supremo (Android)

Jogo de batalha de piões, pronto para virar APK. Roda 100% offline (sem permissão de internet),
em tela cheia, orientação vertical, com o progresso salvo no aparelho e botão Voltar tratado
(fecha menus, pausa a luta; no menu principal sai do app).

**Este pacote é o código-fonte. O APK ainda não foi compilado.** Para gerá-lo, use um dos dois caminhos abaixo.

## Caminho 1: GitHub gera o APK para você (sem instalar nada)

Faça no computador (o upload de pastas do GitHub não funciona direito no celular).

1. Crie uma conta em github.com e um repositório novo, vazio (pode ser privado).
2. Extraia este zip. No repositório, clique em **Add file > Upload files** e arraste **todo o conteúdo**
   da pasta extraída, incluindo a pasta oculta `.github`. Clique em **Commit changes**.
3. Abra a aba **Actions**. O workflow **Build APK** começa sozinho (leva uns 5 minutos).
   Se não começar, escolha **Build APK > Run workflow**.
4. Quando ficar verde, abra a execução e baixe **giro-supremo-apk** em *Artifacts*.
   Dentro do zip está o `app-debug.apk`.

## Caminho 2: Android Studio

1. Instale o Android Studio e abra esta pasta (**Open**). Aguarde o *Gradle Sync*.
2. Menu **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
3. O arquivo fica em `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar no celular (Poco X7 Pro)

1. Passe o `app-debug.apk` para o celular (cabo, Google Drive, Telegram etc.).
2. Abra o arquivo. Quando o Android pedir, permita **instalar apps desconhecidos** para o app que você usou para abrir.
3. Toque em **Instalar**. O ícone "Giro Supremo" aparece na tela inicial.

O APK é assinado com a chave de depuração do Android, o que basta para instalar e jogar.
Ele não serve para publicar na Play Store.

## Onde mexer

- Nome do app: `app/src/main/res/values/strings.xml`
- Jogo (HTML, CSS e JS num arquivo só): `app/src/main/assets/index.html`
- Ícone: `app/src/main/res/mipmap-*`
- Versão e pacote: `app/build.gradle`
