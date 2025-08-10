Durante toda história da Rocketseat existem duas perguntas que as pessoas mais me fazem, o tema do meu VSCode (que é o Dracula) e as configurações do meu terminal de desenvolvimento.
Antes de mais nada, nesse post vou considerar que você esteja utilizando Unix (Mac ou Linux) já que no Windows fica bem inviável configurar o que eu menciono nesse post a não ser que você crie um subsistema Linux dentro dele.
A minha ideia com esse post é mostrar exatamente todas configurações que faço em meu terminal como tema, plugins, configurações, etc.
Instalando Zsh
Antes de conseguirmos iniciar com qualquer configuração precisamos instalar o Zsh. Como existem várias formas de instalação dependendo do sistema operacional que você está, leia esse guia: https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH
Com o Zsh instalado deve ser possível você executar:
zsh --version
E receber algo como: zsh 5.9 (x86_64-apple-darwin22.0).
Fique pode dentro dos temas que usamos por aqui clicando aqui
Instalando Oh My Zsh
Para instalar o Oh My Zsh você precisa executar o comando abaixo (você deve ter o cURL instalado para executa-lo):
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
A partir de agora todas configurações que você quer fazer como adicionar variáveis ambientes ou configurar seu terminal de qualquer forma utilize o arquivo ~/.zshrc e não mais o ~/.bash_profile ou derivados.
Agora reiniciando seu terminal você deve ter algo diferente do convencional, parecido com isso:
Lembrando que a ainda vamos realizar configurações de cores, informações que aparecem em tela, etc.
Utilizando Dracula
Dracula é um padrão de cores disponível para muitas aplicações de desenvolvimento e hoje utilizo esse esquema em boa parte dos apps em que desenvolvo.
O Dracula está disponível para muitos terminais e você pode conferir todos aqui: https://draculatheme.com na seção "Terminal".
Se você estiver no Mac usando o Terminal padrão, provavelmente irá usar: https://draculatheme.com/terminal/
Se você estiver no Linux com uma distribuição que usa Gnome, vai utilizar: https://github.com/dracula/gnome-terminal
Tema Spaceship
Agora vamos instalar o tema Spaceship que vai modificar um pouco as informações que são exibidas no terminal, com ele podemos mostrar a versão do Node atual, do Docker, etc.
Instalando FiraCode
Antes de iniciar a configuração do Spaceship precisamos instalar a fonte Fira Code que possui diversos ícones dos quais são utilizados nesse tema. Baixe o zip da última versão da fonte disponível aqui: https://github.com/tonsky/FiraCode/releases
Descompacte o arquivo baixado e na pasta TTF copie os arquivos de fonte para as fontes do seu sistema (cada sistema operacional possui uma forma de fazer isso).
Depois disso será necessário configurar seu terminal com essa fonte.
Instalando Spaceship
Vamos começar clonando o repositório do Spaceship em nossa pasta de themes do Oh My Zsh (é necessário ter instalado o Git pra isso):
git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
Agora vamos criar um link simbólico para o arquivo do tema do Spaceship na pasta dos temas do Oh My Zsh:
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
Agora dentro do arquivo ~/.zshrc vamos alterar a variável ZSH_THEME ficando dessa forma:
ZSH_THEME="spaceship"
Agora reinicie o terminal e você verá uma interface bem mais limpa.
Configurações adicionais
A partir de agora você já finalizou todas instalações e tudo a partir de aqui são preferências minhas que gosto de utilizar em meu terminal, por isso fique à vontade para incluir/excluir qualquer item abaixo.
Proximos passos:
Agora é a vez do seu Editor de código ser turbinado leia: Dominando o VS Code: guia para aumentar sua produtividade
Vamos ver como os comandos docker ficam nessa configuração? Leia: Docker: os comandos mais utilizados
Configurando Spaceship
Por mais que seja muito interessante mostrar as versões do Node, Docker e outros itens no nosso terminal geralmente isso consome processamento e pode tornar mais lento o carregamento de pastas, por isso eu gosto de desabilitar a maioria dessas opções.
Oferta nunca antes vista de aniversário da RocketseatGaranta 5 anos de acesso pelo menor preço possível e mude sua carreira para sempre.
