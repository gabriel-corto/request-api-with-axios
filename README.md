É inegável a popularidade do NodeJs em quase todas as áreas do desenvolvimento, usa-se node para quase tudo, desde soluções mobile com Reat Native e IONIC, backend de aplicações, ferramentas de linha de comando, até a profunda dependências nos fluxos de desenvolvimento de frontends ricos com VueJs, React e Angular, assim conhecer o entorno de seu ecosistema é essencial. Com isso em mente, resolvi escrever este artigo e deixar um pouco mais mastigado e acessível os principais comandos de seu gerenciador de pacote oficial, o NPM (Node Package Manager), usado extensivamente no dia a dia para gerenciar as dependências do projeto.

Atalhos mais comumns
Comando	Atalho
install	i
list	ls
test	t
–global	-g
–save	-S
–save-dev	-D
Principais Comandos
npm help {COMMAND}
Para se obter o manual do comando

npm install {MODULE}
Ou apenas “npm i {MODULE}“, é usado para instalar dependências

Executar apenas “npm install“ instala todas as dependências configuradas no arquivos package.json;
Ao usar a flag “--production“ serão instaladas apenas depedências de produção;
npm remove {MODULE}
Remove um módulo previamente instalado

npm init
Comando usado para iniciar um projeto novo na pasta atual, se utilizado a flag “-y“ assim “npm init -y“ será gerado uma inicialização com os parâmetros default sem questionamentos.

npm ci
Usado para o deploy de aplicações instalando todas as dependência definidas package.json e versões do package-lock.json

Caracteristicas importantes:

Caso a pasta node_modules exista a mesma será removida e recriada na sequência
Esse comando não altera os arquivos package.json e package-lock.json
É requerido que na pasta se tenha o arquivo package-lock.json ou npm-shrinkwrap.json
npm outdated
Retorna a lista de dependências desatualizadas mostrando a versão mais recente suportada pela configuração no package.json e a ultima versão

npm update
Atualiza projetos para a ultima versão respeitando o package.json
Pode-se atualizar um único módulo executando “npm update {MODULE}”

npm version {COMMAND}
Manipula a versão atual do projeto e adiciona tags no projeto git
Comandos disponíveis: {VERSION} | major | minor | patch | premajor | preminor | prepatch | prerelease
Ex: npm version patch ou npm version 1.0.20

npm audit
Executa uma auditoria no projeto para identificar se existe alguma dependência com vulnerabilidade conhecida
Ao utilizar a flag --fix é feita uma tentativa de corrigir o problema de forma automática.

npm list
Ou apenas “npm ls”, lista todas as dependências do projeto
Com a flag “–depth X” podemos ver uma arvore de dependências onde X é a profundidade que se deseja

npm shrinkwrap
Comando usado para travar a versão das dependências do seu projeto
Ao executar esse comando será criado o arquivo npm-shrinkwrap.json que servirá de base para instalação das dependências

npm adduser {USERNAME}
Adiciona um novo usuário no registre para permitir o envio de pacotes para o mesmo

npm publish
Publica o módulo atual no registre configurado

npm home {MODULE}
Abre a página do projeto

npm repo {MODULE}
Abre o repositório de código do projeto`