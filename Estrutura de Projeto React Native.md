# Estrutura de Projeto React Native

Este documento descreve a estrutura de um projeto React Native, oferecendo um guia para organização de arquivos e pastas.


## Estrutura Básica de Pastas

```plaintext
nome_do_aplicativo/
├── android/
│ ├── app/
│ │ ├── src/
│ │ │ ├── main/
│ │ │ │ ├── AndroidManifest.xml
│ │ │ │ ├── java/
│ │ │ │ │ └── com/
│ │ │ │ │ └── exemplo/
│ │ │ │ │ └── nome_do_aplicativo/
│ │ │ │ │ ├── MainApplication.java
│ │ │ │ │ └── MainActivity.java
│ │ │ │ ├── res/
│ │ │ │ │ └── ...
│ │ │ └── ...
│ │ └── build.gradle
│ │ └── ...
│ └── ...
├── ios/
│ ├── NomeDoAplicativo/
│ │ ├── AppDelegate.m
│ │ ├── Info.plist
│ │ └── ...
│ └── ...
├── src/
│ ├── components/
│ │ ├── Button.js
│ │ ├── Input.js
│ │ └── ... (outros componentes reutilizáveis)
│ ├── screens/
│ │ ├── HomeScreen.js
│ │ ├── LoginScreen.js
│ │ ├── ProfileScreen.js
│ │ └── ... (Telas do aplicativo)
│ ├── navigation/
│ │ ├── AppNavigator.js (ou usando react-navigation)
│ │ └── ...
│ ├── services/
│ │ ├── api.js (ou similar para chamadas de API)
│ │ └── ... (outros serviços)
│ ├── utils/
│ │ ├── helpers.js
│ │ └── ... (funções utilitárias)
│ ├── App.js (componente principal do aplicativo)
│ ├── index.js (ponto de entrada)
│ └── ... (outros arquivos, como reducers para Redux, se usado)
├── assets/
│ ├── images/
│ │ └── ... (imagens)
│ ├── icons/
│ │ └── ... (ícones)
│ └── ...
├── tests/
│ └── ... (testes)
├── .eslintrc.js (configuração do ESLint)
├── .prettierrc.js (configuração do Prettier)
├── babel.config.js
├── metro.config.js
├── package.json
├── .gitignore
└── README.md
```

# Estrutura de Pastas Explicada

* **`nome_do_aplicativo/`:**  Raiz do projeto.
## Descrição das Pastas e Arquivos Principais

* **`android/` e `ios/`:**  Contém os projetos nativos para Android e iOS, respectivamente.  Geralmente, você não precisa modificar esses arquivos diretamente, a menos que precise integrar bibliotecas nativas ou funcionalidades específicas da plataforma.

* **`src/`:**  O coração do seu aplicativo React Native. Contém todo o código JavaScript.
    * **`components/`:** Componentes reutilizáveis da UI.
    * **`screens/`:** Telas do aplicativo.
    * **`navigation/`:**  Lógica de navegação.
    * **`services/`:**  Serviços como chamadas de API, acesso a banco de dados, etc.
    * **`utils/`:** Funções utilitárias.
    * **`App.js`:** Componente raiz do aplicativo.
    * **`index.js`:** Ponto de entrada.

* **`assets/`:** Imagens, ícones e outros recursos estáticos.

* **`__tests__/`:**  Testes unitários e de integração.

* **`.eslintrc.js`:** Configuração do ESLint para garantir a qualidade do código.

* **`.prettierrc.js`:** Configuração do Prettier para formatar o código automaticamente.

* **`babel.config.js` e `metro.config.js`:** Configurações do Babel e Metro.

* **`package.json`:**  Gerencia as dependências do projeto e scripts.

* **`.gitignore`:** Lista de arquivos e pastas que devem ser ignorados pelo Git.

* **`README.md`:**  Documentação do projeto (**essencial!**).

## Iniciar um Projeto (com Expo)

1. **Instale o Expo CLI:** `npm install -g expo-cli`
2. **Crie um novo projeto:** `expo init nome_do_aplicativo` (escolha um template).
3. **Navegue até o projeto:** `cd nome_do_aplicativo`
4. **Inicie o aplicativo:** `expo start`

## Bibliotecas Recomendadas

* **`react-navigation`:** Para navegação entre telas.
* **`redux` (opcional):** Para gerenciamento de estado complexo.


Este arquivo `README.md` fornece uma visão geral da estrutura do projeto e serve como ponto de partida para o desenvolvimento.  Mantenha-o atualizado conforme o projeto evolui!
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
IGNORE_WHEN_COPYING_END

Para gerar a saída, copie o código Markdown acima e cole em um arquivo chamado README.md na raiz do seu projeto. Você pode então visualizar este arquivo no GitHub ou em qualquer editor de Markdown.

Lembre-se de customizar o README.md com informações específicas do seu projeto, como descrição, instruções de instalação, contribuição, licença, etc. Um bom README é fundamental para a documentação e colaboração em qualquer projeto de software.