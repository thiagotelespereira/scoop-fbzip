# scoop-fbzip
App manifest para instalação do sotware fbzip via scoop.

## O que é o fbzip
Freebyte Zip é um programa confiável, potente e gratuito zip/unzip para o Windows 7, XP, Vista, 200x, NT, 9x, Linux/wine e todas as edições de 64 bits do Windows. O programa permite compactar e descompactar arquivos, criar arquivos zip, proteger arquivos com senha, visualizar, ordenar e criptografar o conteúdo do arquivo zip, e também fazer arquivos self.extracting. Este programa é o sucessor direto para o programa HJ-Zip. O programa é de apenas 300 Kb de tamanho, e não requer qualquer tipo de instalação.

O Freebyte Zip roda também via command line.

Saiba mais sobre o fbzip em: [http://www.freebyte.com/fbzip][1]

## Como instalar
Adicione o app manifest ao bucket do scoop executando o seguinte comando:

`scoop bucket add fbzip https://gist.github.com/thiagotelespereira/82c3999edbaf2ea74a3ea59860782831`

Uma vez adicionado ao seu bucket, o aplicativo já estará pronto para ser instalado. Para instalar basta executar o seguinte comando:

`scoop install fbzip`

>**Nota importante**
>
>Para instalar corretamente o aplicativo fbzip, você deverá mudar o diretório de instalação manuallmente para o seguinte caminho: `~AppData\Local\scoop\apps\fbzip\2.3.1`. Caso o aplicativo seja instalado em outro local, o mesmo não irá funcionar.

## Utilizando o fbzip via command line

###Command line

`fbzip.exe [opções] <nome do arquivo zip> <endereço absoluto>`

- <endereço absoluto> : pode conter nomes de arquivos, diretórios ou wildcards.

### Opções

- -e: descompactar arquivos
- -a: compactar arquivos
- -p: utiliza o path atual para descompactar os arquivos (cria diretórios se necessário)
- -p: armazena a informação do diretório quando for compactar os arquivos
- -r: compacta recursivamente os subdiretórios

### Exemplos

**Compactando múltiplos arquivos**

`fbzip.exe -a -p -r "C:\compactado.zip" "F:\arquivos\doc01.doc" "F:\arquivos\doc02.doc" "F:\fotos\picture.jpg" "F:\backup"`

Será criado um arquivo zip nomeado como *Compactado.zip*, contendo todos os arquivos informados. O diretório *backup* será compactado de maneira recursiva, e as informações sobre os caminhos serão armazenadas no arquivo zip.

**Descompactando**

`fbzip.exe -e -p "c:\compactado.zip" "F:\data\backup\"`



[1]: http://www.freebyte.com/fbzip