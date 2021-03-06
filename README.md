# Etapas para rodar o projeto 

## Descrição 

## Pré-requisitos

- Android Studio
- Java 8
- JAVA_HOME e ANDROID_HOME configurados
- Ruby
- Appium
- Genymotion (opcional)

## Passo a passo para instalações

### 01. Android Studio 

1. Instalar o android studio https://developer.android.com/studio/index.html?hl=pt-br 
2. Configurar o JAVA_HOME e ANDROID_HOME

### 02. Ruby 

1. Instalar o Ruby https://rubyinstaller.org/downloads/ com a versão mais estável 

2. Após instalar verificar a versão do ruby 
```
ruby --version
```
3. Pelo cmd instalar o pacote adicionar do ruby com o comando e selecionar a opção 3 

```
ridk install
``` 

4. Instalar bundler pelo cmd 

```
gem install bundler
``` 

5. verificar versão do bundler 

```
bundler --version
```

### 03. Emulador
1. Realizar download do Genymotion com o virtualBox https://www.genymotion.com/download/

### 04. Appium - windows

1. Na raiz do computador criar a pasta para o projeto 
```
C:\nome da pasta\
```
2. Criar a pasta do appium dentro da pasta criada
```
C:\nome da pasta do projeto\adicionar
```
3. Instalar o appium e appium-doctor como admin 
```
npm install -g appium
npm install -g appium-doctor 
```
4. inserir o comando bundler install para adicionar todas as dependencias vinculadas ao arquivo Gemfile

5. remover o pacote eventmachine para instalar corretamente 
```
gem uninstall eventmachine
```
6. instalar pacote corretamente
```
gem install eventmachine --platform ruby
```
7. Após realizar a instalação de todos as dependencias necessárias rodar o 
``` 
appium-doctor --android
```
para verificar se não está faltando nada no computador.

## Executar projeto

### Subir aplicação 

1. Abrir o Genymotion e esperar carregar o device 

2. Com o promt aberto e com permissão de administrar, rodar o comando abaixo para verificar o id do device emulado 

 ```
 adb devices
 ``` 
necessário para utilizar no arquivo ```appium.tx```.

3. Dentro do projeto existe a pasta apk que contém o  apk para ser realizado o teste.

4. No arquivo appium.txt, possui todas as caps necessárias para subir a aplicação 

5. Com o comando abaixo pelo cmd a aplicação irá subir

```
appium
``` 
 
6. Pelo cmd dentro da pasta que está o arquivo ```appium.tx``` e o apk,inserir o comando 
```
Arc
```

### Como escrever novos cenários 

1. Pela linha de comando na raiz do projeto escreva o comando a baixo, ele irá criar a estrutura de pastas, para a escrita do cenário

```
cucumber --init
``` 

2. Para receber os steps prontos, após criar a feature apenas digite no cmd o comando abaixo no cmd e ele irá te passar o step. 

```
cucumber
```

### Rodar Cenarios


1. Para rodar um cenário especifico, é só adicionar a @tag do projeto 

```
cucumber -t @tag 
```

2. Para rodar todos os cenários 

```
cucumber
```

3. Rodar teste e gerar 

3.1 Cucumber Report no final 

```
cucumber -t @tag --format html --out log/cenarioName.html
```

3.2 Report html 

    ```
    cucumber -t @tag 
    ```


