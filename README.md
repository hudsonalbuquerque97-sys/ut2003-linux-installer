# 🎮 Unreal Tournament 2003 - Linux Installer

<div align="center">

![Unreal Tournament 2003](https://img.shields.io/badge/UT2003-Installer-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Linux-blue?style=for-the-badge&logo=linux)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Languages](https://img.shields.io/badge/Languages-PT%20|%20EN-yellow?style=for-the-badge)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Bash](https://img.shields.io/badge/bash-5.0%2B-green.svg)
![Platform](https://img.shields.io/badge/platform-Linux-orange.svg)
![Ubuntu](https://img.shields.io/badge/Ubuntu-compatible-red.svg)
![Linux Mint](https://img.shields.io/badge/linux%20mint-compatible-green)
![Debian](https://img.shields.io/badge/Debian-compatible-pink.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**Instalador automatizado e bilíngue (PT-BR/EN) para Unreal Tournament 2003 no Linux**

[English](#-english) | [Português](#-português)

</div>

---

## ⚠️ AVISO IMPORTANTE / IMPORTANT NOTICE

<div align="center">

### 🚫 Este script NÃO fornece o jogo / This script does NOT provide the game

**Este é apenas um instalador/configurador automático**  
*This is only an automatic installer/configurator*

Você precisa ter uma cópia original do jogo (CD/DVD/ISO)  
*You need to have an original copy of the game (CD/DVD/ISO)*

</div>

---

## 🇧🇷 Português

### 📋 O que este script faz?

Este script automatiza completamente a instalação e configuração do Unreal Tournament 2003 no Linux, realizando:

- ✅ **Extração automática** dos arquivos do jogo (ISO/DVD ou pasta)
- ✅ **Aplicação do patch 2225.3** (última versão oficial)
- ✅ **Configuração do ambiente Linux** (OpenGL, SDL)
- ✅ **Correção de bibliotecas** de som (SDL, OpenAL)
- ✅ **Criação de atalhos** no menu de aplicativos
- ✅ **Configuração de CD Key** padrão
- ✅ **Descompressão de arquivos .uz2**
- ✅ **Criação de launcher** no sistema
- ✅ **Configuração automática** de renderização
- ✅ **Interface bilíngue** (detecta idioma do sistema)
- ✅ **Limpeza de arquivos temporários** da instalação original

### 🎯 Recursos

- 🌍 **Detecção automática de idioma** (PT-BR/EN)
- 🔧 **Instalação totalmente automatizada** com zero interação
- 📦 **Verifica e instala dependências** automaticamente
- 🎨 **Converte e instala ícones** para o sistema
- 🔑 **CD Key pré-configurado** (pode ser alterado depois)
- 🎮 **Criação de executável global** (`ut2003` no terminal)
- 🗂️ **Suporte múltiplas fontes**: ISO, DVD montado, ou pasta de arquivos
- 🧹 **Remove arquivos desnecessários** (temp, cache, instaladores Windows)

### 📦 Tipos de Arquivos Suportados

O script aceita os seguintes formatos de origem:

#### 1️⃣ Arquivo ISO do DVD
```
/caminho/para/arquivo.iso
/caminho/para/arquivo.ISO
```

#### 2️⃣ Pasta com arquivos do DVD
```
/caminho/para/pasta/ut2003
```

#### 3️⃣ Conteúdo dos 3 CD-ROMs combinados
Se você tem a versão em 3 CDs:
1. Copie **TODO** o conteúdo do CD 1 para uma pasta
2. Copie **TODO** o conteúdo do CD 2 para a **MESMA** pasta (sobrescreva arquivos)
3. Copie **TODO** o conteúdo do CD 3 para a **MESMA** pasta (sobrescreva arquivos)
4. Informe o caminho dessa pasta única ao script

### ⚠️ IMPORTANTE: Formato do Caminho

❌ **NÃO use aspas** ao informar o caminho:
```bash
# ERRADO:
"/home/usuario/jogos/ut2003.iso"
'/home/usuario/jogos/ut2003.iso'

# CORRETO:
/home/usuario/jogos/ut2003.iso
```

✅ **Use caminhos absolutos ou relativos** sem aspas:
```bash
# Exemplos corretos:
/home/usuario/Documentos/UT2003.iso
~/Downloads/ut2003.iso
./ut2003/
../jogos/ut2003.iso
```

### 🚀 Como Usar

#### Pré-requisitos
- Ubuntu/Debian ou derivados (64-bit)
- Acesso à internet (para baixar o patch)
- Cópia original do UT2003 (CD/DVD/ISO)
- Pelo menos 2GB de espaço livre

#### Instalação

1. **Baixe o script:**
```bash
wget https://raw.githubusercontent.com/hudsonalbuquerque97-sys/ut2003-linux-installer/refs/heads/main/ut2003_intaller.sh

ut2003_installer.sh
```

2. **Torne-o executável:**
```bash
chmod +x ut2003_installer.sh
```

3. **Execute:**
```bash
./ut2003_installer.sh
```

4. **Siga as instruções** na tela e informe o caminho da ISO ou pasta (sem aspas!)

#### Após a Instalação

O jogo pode ser executado de várias formas:

```bash
# Via executável global
ut2003

# Via launcher
~/Games/ut2003/ut2003_launch.sh

# Via comando direto
cd ~/Games/ut2003/System && ./ut2003-bin

# Via menu de aplicativos (procure por "Unreal Tournament 2003")
```

### 🔧 Dependências

O script verifica e instala automaticamente:

- `wget` - Download do patch
- `util-linux` - Suporte 32-bit
- `expect` - Automação de instalação
- `imagemagick` - Conversão de ícones
- `libstdc++5:i386` - Biblioteca C++ 32-bit
- `libsdl1.2debian:i386` - Biblioteca SDL para som
- `libopenal1:i386` - Biblioteca OpenAL para áudio 3D

### 📁 Estrutura de Instalação

```
~/Games/ut2003/           # Diretório principal do jogo
├── System/               # Executáveis e bibliotecas
├── Maps/                 # Mapas do jogo
├── Textures/             # Texturas
├── Sounds/               # Sons
├── Music/                # Músicas
└── ut2003_launch.sh      # Launcher do jogo

~/.ut2003/                # Configurações do usuário
└── System/
    ├── UT2003.ini        # Configuração principal
    └── User.ini          # Configuração do usuário

~/.local/share/applications/
└── ut2003.desktop        # Atalho do menu

/usr/local/bin/
└── ut2003                # Executável global
```

### 🎨 Personalização

#### Alterar CD Key
Edite o arquivo:
```bash
nano ~/Games/ut2003/System/cdkey
```

#### Modificar configurações
```bash
nano ~/.ut2003/System/UT2003.ini
nano ~/.ut2003/System/User.ini
```

### 🐛 Solução de Problemas

#### O jogo não inicia
```bash
# Verifique as bibliotecas
cd ~/Games/ut2003/System
ldd ./ut2003-bin

# Reinstale dependências
sudo apt-get install --reinstall libstdc++5:i386 libsdl1.2debian:i386 libopenal1:i386
```

#### Sem som
```bash
cd ~/Games/ut2003/System
ln -sf /usr/lib/i386-linux-gnu/libSDL-1.2.so.0 libSDL-1.2.so.0
ln -sf /usr/lib/i386-linux-gnu/libopenal.so.1 openal.so
```

#### Problemas de permissão
```bash
chmod -R 775 ~/Games/ut2003
chmod -R 775 ~/.ut2003
```

---

## 🇺🇸 English

### 📋 What does this script do?

This script completely automates the installation and configuration of Unreal Tournament 2003 on Linux, performing:

- ✅ **Automatic extraction** of game files (ISO/DVD or folder)
- ✅ **Application of patch 2225.3** (latest official version)
- ✅ **Linux environment configuration** (OpenGL, SDL)
- ✅ **Sound library fixes** (SDL, OpenAL)
- ✅ **Creation of shortcuts** in the applications menu
- ✅ **Default CD Key configuration**
- ✅ **Decompression of .uz2 files**
- ✅ **System launcher creation**
- ✅ **Automatic rendering configuration**
- ✅ **Bilingual interface** (detects system language)
- ✅ **Cleanup of temporary files** from original installation

### 🎯 Features

- 🌍 **Automatic language detection** (PT-BR/EN)
- 🔧 **Fully automated installation** with zero interaction
- 📦 **Checks and installs dependencies** automatically
- 🎨 **Converts and installs icons** for the system
- 🔑 **Pre-configured CD Key** (can be changed later)
- 🎮 **Global executable creation** (`ut2003` in terminal)
- 🗂️ **Multiple source support**: ISO, mounted DVD, or file folder
- 🧹 **Removes unnecessary files** (temp, cache, Windows installers)

### 📦 Supported File Types

The script accepts the following source formats:

#### 1️⃣ DVD ISO File
```
/path/to/file.iso
/path/to/file.ISO
```

#### 2️⃣ Folder with DVD Files
```
/path/to/folder/ut2003
```

#### 3️⃣ Combined Content of 3 CD-ROMs
If you have the 3-CD version:
1. Copy **ALL** content from CD 1 to a folder
2. Copy **ALL** content from CD 2 to the **SAME** folder (overwrite files)
3. Copy **ALL** content from CD 3 to the **SAME** folder (overwrite files)
4. Provide the path to this single folder to the script

### ⚠️ IMPORTANT: Path Format

❌ **DO NOT use quotes** when providing the path:
```bash
# WRONG:
"/home/user/games/ut2003.iso"
'/home/user/games/ut2003.iso'

# CORRECT:
/home/user/games/ut2003.iso
```

✅ **Use absolute or relative paths** without quotes:
```bash
# Correct examples:
/home/user/Documents/UT2003.iso
~/Downloads/ut2003.iso
./ut2003/
../games/ut2003.iso
```

### 🚀 How to Use

#### Prerequisites
- Ubuntu/Debian or derivatives (64-bit)
- Internet access (to download the patch)
- Original copy of UT2003 (CD/DVD/ISO)
- At least 2GB of free space

#### Installation

1. **Download the script:**
```bash
https://raw.githubusercontent.com/hudsonalbuquerque97-sys/ut2003-linux-installer/refs/heads/main/ut2003_intaller.sh

ut2003_installer.sh
```

2. **Make it executable:**
```bash
chmod +x ut2003_installer.sh
```

3. **Run it:**
```bash
./ut2003_installer.sh
```

4. **Follow the on-screen instructions** and provide the path to the ISO or folder (without quotes!)

#### After Installation

The game can be run in several ways:

```bash
# Via global executable
ut2003

# Via launcher
~/Games/ut2003/ut2003_launch.sh

# Via direct command
cd ~/Games/ut2003/System && ./ut2003-bin

# Via applications menu (search for "Unreal Tournament 2003")
```

### 🔧 Dependencies

The script automatically checks and installs:

- `wget` - Patch download
- `util-linux` - 32-bit support
- `expect` - Installation automation
- `imagemagick` - Icon conversion
- `libstdc++5:i386` - 32-bit C++ library
- `libsdl1.2debian:i386` - SDL library for sound
- `libopenal1:i386` - OpenAL library for 3D audio

### 📁 Installation Structure

```
~/Games/ut2003/           # Main game directory
├── System/               # Executables and libraries
├── Maps/                 # Game maps
├── Textures/             # Textures
├── Sounds/               # Sounds
├── Music/                # Music
└── ut2003_launch.sh      # Game launcher

~/.ut2003/                # User settings
└── System/
    ├── UT2003.ini        # Main configuration
    └── User.ini          # User configuration

~/.local/share/applications/
└── ut2003.desktop        # Menu shortcut

/usr/local/bin/
└── ut2003                # Global executable
```

### 🎨 Customization

#### Change CD Key
Edit the file:
```bash
nano ~/Games/ut2003/System/cdkey
```

#### Modify settings
```bash
nano ~/.ut2003/System/UT2003.ini
nano ~/.ut2003/System/User.ini
```

### 🐛 Troubleshooting

#### Game won't start
```bash
# Check libraries
cd ~/Games/ut2003/System
ldd ./ut2003-bin

# Reinstall dependencies
sudo apt-get install --reinstall libstdc++5:i386 libsdl1.2debian:i386 libopenal1:i386
```

#### No sound
```bash
cd ~/Games/ut2003/System
ln -sf /usr/lib/i386-linux-gnu/libSDL-1.2.so.0 libSDL-1.2.so.0
ln -sf /usr/lib/i386-linux-gnu/libopenal.so.1 openal.so
```

#### Permission issues
```bash
chmod -R 775 ~/Games/ut2003
chmod -R 775 ~/.ut2003
```

---

## 📝 Notas Técnicas / Technical Notes

### CD Key Padrão / Default CD Key
```
LYR22-RZ743-A9D7T-CNNEN
```
Este é um CD Key genérico para testes. Se você possui uma cópia original, use sua própria chave.

*This is a generic CD Key for testing. If you own an original copy, use your own key.*

### Compatibilidade / Compatibility

Testado em / Tested on:
- ✅ Ubuntu 20.04 LTS
- ✅ Ubuntu 22.04 LTS
- ✅ Ubuntu 24.04 LTS
- ✅ Debian 11 (Bullseye)
- ✅ Debian 12 (Bookworm)
- ✅ Linux Mint 21+
- ✅ Pop!_OS 22.04+

### Limitações Conhecidas / Known Limitations

- ⚠️ Requer arquitetura 64-bit com suporte a 32-bit / Requires 64-bit architecture with 32-bit support
- ⚠️ Algumas distribuições podem precisar de configuração adicional do multilib / Some distributions may need additional multilib configuration
- ⚠️ Placas de vídeo muito antigas podem ter problemas com OpenGL / Very old graphics cards may have OpenGL issues

---

## 🤝 Contribuindo / Contributing

Contribuições são bem-vindas! Sinta-se à vontade para:

*Contributions are welcome! Feel free to:*

- 🐛 Reportar bugs / Report bugs
- 💡 Sugerir melhorias / Suggest improvements
- 🔧 Enviar pull requests / Submit pull requests
- 📖 Melhorar a documentação / Improve documentation

---

## 📜 Licença / License

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.

*This project is licensed under the MIT License - see the LICENSE file for details.*

---

## 🙏 Agradecimentos / Acknowledgments

- Epic Games - Por criar o Unreal Tournament 2003
- Comunidade Linux Gaming - Pelo suporte contínuo
- Josh Barrass - Pelo patch 2225.3 para Linux

---

<div align="center">

### ⭐ Se este projeto te ajudou, considere dar uma estrela!

### *If this project helped you, consider giving it a star!*

---

💖 **Feito com amor para a comunidade gamer Linux**

💖 **Made with love for the Linux gaming community**

---

🎮 **Game On!** 🐧

</div>
