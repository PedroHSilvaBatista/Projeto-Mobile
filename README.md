# 📱 FIAP — React Native (Expo)

## Aula: Login + Navegação

Este projeto foi desenvolvido em aula com o objetivo de ensinar os conceitos fundamentais de **React Native com Expo**, focando em:

* Criação de projeto
* Organização de pastas
* Construção de telas
* Navegação entre telas
* Componentização básica

---

# 🎯 Objetivo

Construir uma aplicação simples contendo:

* Tela de Login
* Tela de Cadastro
* Tela de Recuperação de Senha
* Tela Home
* Navegação entre telas (Stack)

> ⚠️ Este projeto NÃO possui backend.
> O foco é **layout + navegação**.

---

# 🧱 Tecnologias utilizadas

* React Native
* Expo (SDK 54)
* React Navigation

---

# 🚀 Como executar o projeto

## 1. Clonar o repositório

```bash
git clone https://github.com/helofleury/Auth_Firebase.git
```

## 2. Acessar a pasta

```bash
cd fiap-auth-app
```

## 3. Instalar dependências

```bash
npm install
```

## 4. Rodar o projeto

```bash
npx expo start
```

---

# 📦 Instalação manual (caso necessário)

Se precisar recriar o projeto do zero:

```bash
npx create-expo-app fiap-auth-app --template blank@54
```

Instalar navegação:

```bash
npm install @react-navigation/native
npm install @react-navigation/native-stack
npm install react-native-screens@4.16.0 --save-exact
npx expo install react-native-safe-area-context
```

---

# 📁 Estrutura do projeto

```text
src/
  components/
  navigation/
    AppNavigator.js
  screens/
    LoginScreen.js
    RegisterScreen.js
    ForgotPasswordScreen.js
    HomeScreen.js
```

---

# 🧭 Fluxo de navegação

* Login → Home
* Login → Cadastro
* Login → Esqueci minha senha
* Cadastro → Voltar
* Esqueci senha → Voltar
* Home → Login

---

# 📸 Telas do app

* Login
* Cadastro
* Recuperação de senha
* Home

---

# 🧠 Conceitos abordados

* `View`, `Text`, `TextInput`, `Button`
* `TouchableOpacity`
* `StyleSheet`
* Navegação com Stack
* Props e navegação (`navigation.navigate`)
* Organização de projeto
* Componentização básica

---

# 🛠️ Problemas comuns

## Erro: "expected dynamic type 'boolean', but had type 'string'"

Solução aplicada:

* Fixar versão:

```bash
npm install react-native-screens@4.16.0 --save-exact
```

---

# 🎯 Próximos passos

* Melhorar layout (UI/UX)
* Criar componentes reutilizáveis
* Adicionar validação de formulário
* Integrar com Firebase (login real)
* Persistência de usuário

---

# 🔧 Melhorias Implementadas

As seguintes melhorias foram aplicadas ao projeto após a aula inicial:

## Melhoria 1 — Formatação do preço no padrão brasileiro
O campo de preço agora formata automaticamente o valor enquanto o usuário digita,
seguindo o padrão brasileiro (ex: R$ 1.299,99).

**Arquivo alterado:** `src/screens/HomeScreen.js`

## Melhoria 2 — Teclado sobrepondo campos de texto
Adicionado o componente `KeyboardAvoidingView` nas telas que possuem campos de texto,
evitando que o teclado sobreponha os inputs em telas menores.

**Arquivos alterados:**
* `src/screens/HomeScreen.js`
* `src/screens/LoginScreen.js`
* `src/screens/RegisterScreen.js`
* `src/screens/ForgotPasswordScreen.js`

## Melhoria 3 — Preservar dados ao abrir o leitor de código de barras
Ao navegar para a tela do leitor de código de barras, os dados já preenchidos
(nome e preço do produto) agora são preservados ao retornar para a tela Home.

**Arquivos alterados:**
* `src/screens/HomeScreen.js`
* `src/screens/BarcodeScannerScreen.js`

## Melhoria 4 — Rolagem da tela em dispositivos menores
Substituída a estrutura de rolagem da tela Home por `ScrollView` + `FlatList` com
`scrollEnabled={false}`, garantindo que todo o conteúdo seja acessível em telas menores.

**Arquivo alterado:** `src/screens/HomeScreen.js`

---

# Conexão

const firebaseConfig = { 

  // apiKey: 'SUA_API_KEY', 
  // authDomain: 'SEU_AUTH_DOMAIN', 
  // projectId: 'SEU_PROJECT_ID', 
  // storageBucket: 'SEU_STORAGE_BUCKET', 
  // messagingSenderId: 'SEU_MESSAGING_SENDER_ID', 
  // appId: 'SEU_APP_ID', 
  // databaseURL: 'SUA_DATABASE_URL', 
}; 

---

# 🗣️ Observação final

Este projeto tem fins educacionais e foi construído passo a passo em aula para facilitar o aprendizado dos alunos.

---

# 👨‍🏫 Autor

Projeto utilizado em aula — FIAP
Professor: Luiz Camilo

---
