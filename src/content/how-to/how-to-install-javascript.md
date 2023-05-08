---
title: "How to install javascript"
subtitle: "Every good web developer needs to run Javacript on it's developing machine, here's how to make your System Javascript ready."
tags: ["javascript", "nodejs", "install", "windows", "macos", "linux"]
date: "2023-03-27T16:36:30+00:00"
authors: ["Javier Seiglie"]
---

[Learn how to code in Javascript](https://4geeks.com/lesson/what-is-javascript-learn-to-code-in-javascript) is an excellent option for those who want to get started in the coding world. Javascript is a versatile and widely used programming language, which makes it a handy tool for any web developer. If you got to this point and still don't know javascript in detail, I invite you to read this guide related to [what is Javascript used for](). Because Javascript is a programming language that runs mainly in browsers (Chrome, Mozilla, Edge, etc.), if we want to use it in the system, we must install NodeJS.

![NodeJs](https://i.imgur.com/zPghTHs.png)

## What is NodeJs?

When we talk about installing Javascript in our system, we mean installing the environment that allows us to develop in Javascript and right there is where we found NodeJs.

NodeJs is the execution environment for Javascript that's used for the development of web apps [Front End](https://4geeks.com/lesson/what-is-front-end-development) and [Back End](https://4geeks.com/lesson/backend-developer). It was created with the version 8 of the engine that Chrome uses to process Javascript code (let's remember that this language is designed to be executed in browsers)

## How to install Javascript (NodeJs)

The first step to add NodeJs to our system would be to access to [this link](https://nodejs.org/es/download) and select the Operative System to start the loading.

![Instalar NodeJS](https://i.imgur.com/8eIqVlp.png)

### Windows

To complete the installation in Windows, you must follow the steps described in the installer. It doesn't require any configuration while it's installing, so it will be "following", "following", "following", "end".

To verify it has been installed correctly:
- We access to the command line (search in CMD applications or press `win` + `r` and type `cmd`)
- Type `node --version`

If installed correctly, it should appear a response similar to the one shown below.

```cmd
v18.15.0
```

### MacOS

#### Installing NodeJs through download from nodejs.org

Once we access to the download area (the link above), we must select `macOS installer` and download it. 

Beacuse it doesn't require any type of modification while installing, you will only have to start the installer and follow the steps ("following", "following", "following", "end".)

#### Installing NodeJs through homebrew

If you want to do the installation from the terminal, you can do it via you could do it through the **homebrew** package manager.

To do the installation we must execute the following command on the terminal

```bash
brew install node
```

#### Installing NodeJs through MacPorts

To install NodeJs using **MacPorts** as a package manager, you will have to open the terminal and type

```bash
sudo port install nodejs
```

To verify the instalation, either by downloading from NodeJs, Homebrew or MacPorts, you will have to open the terminal and run the following command `node --version`. If it was installed correctly, a mensage simillar to this will be shown: 

```bash
v18.15.0
```

### Linux

Because Linux come in different versions, we will talk about how to install NodeJs install NodeJs on Ubuntu only.

#### Install NodeJs with APT

> Important note: Because we will be using the **Super user** to do the installations, you will most likely be asked for your password to complete the steps.

Every time that we are going to add a new software to our system based on Linux, we must update our 
local package indexes and then we can install the package that we want, in this case `nodejs`.

```bash
sudo apt update
sudo apt upgrade
sudo apt install nodejs
```

We have to install **npm** (Node Package Manager) to manage the NodeJs packages, because it doesn't come included in the version described.

```bash
sudo apt install npm
```

#### Install NodeJs with APT and PPA NodeSource

If we want to install a different version of NodeJs to the one we can install with the previous resource, we can use a PPA (Personal Package Archive) mantaine

Si queremos instalar una versión diferente de NodeJs a la que podemos instalar con el recurso anterior, podemos utilizar un PPA (Personal Package Archive) mantenido por NodeSource. En los PPA se encuentran más versiones del paquete que en los repositorios de Ubuntu.

Como mencionamos anteriormente, es necesario realizar un **update** y un **upgrade** siempre que queramos instalar nuevos paquetes para optimizar la compatibilidad de los paquetes y estar usando la versión mas  reciente de nuestros programas y sistemas.

```bash
sudo apt update
sudo apt upgrade
sudo apt-get install curl
```

Si por algun motivo no tenemos instalado **cURL**, lo podemos instalar de la siguiente forma

```bash
sudo apt-get install curl
```

Ahora estamos listos para añadir el repositorio de NodeJs, recuerda cambiar `setup_18.x` por la versión que desees instalar, ejemplo `setup_14.x' 

```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```

Una vez que se haya añadido el repositorio de nuestra elección, debemos de proceder a instalar.

```bash
sudo apt-get install nodejs
```

De esta forma no es necesario instalar **NPM** ya que viene incluido en el paquete que acabamos de instalar.

#### Verificar instalación

Para verificar la instalación de NodeJs y NPM en Linux, abriremos una terminal y escribiremos

```bash
node --version
npm --version
```
De haberse instalado correctamente, se mostrará la siguiente información, para NodeJs `v18.15.0` y para NPM `9.5.0`. Ambos retornos dependerán de la versión instalada. Del mismo modo, podemos usar el comando:

```bash
whereis node
whereis npm
```
Con estos comandos conoceremos donde están instalados los paquetes.

## Ejecutar JavaScript

NodeJs no posee una Interfaz de Usuario (UI) para desarrollar, en vez de eso, mediante el uso de IDEs como VS Code, Atom, etc, podemos ejecutar JavaScript haciendo uso del entorno que proporciona NodeJs sin necesidad de realizar grandes cambios (o cambio alguno) en la configuración del Sistema nosotros mismos.

Digamos que tenemos un archivo `app.js` que creamos para probar nuestra instalación y ejecutar código JavaScript desde nuestro sistema.

Este será el código js que estará en nuestro archivo app.js:

```javascript
console.log("I can run now outside of the browser!")
```

Para ejecutar este código, debemos de abrir la terminal o CMD (si estás utilizando Windows) y escribir `node` y seguido donde se encuentra nuestro archivo js que queremos ejecutar.

**Ejemplo** supongamos que tenemos nuestro archivo app.js en la unidad `C:` carpeta `test`

```bash
node c:\test\app.js
```

De haberse pasado la dirección correcta donde se encuentra el archivo, se mostrara en la consola:

```bash
I can run now outside of the browser!
```

Puedes leer contenido relacionado y mucho mas en el blog de [4Geeks](www.4geeks.com/es/how-to).
