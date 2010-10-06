#Minify

Minifica arquivos arquivos __css__ (__.css__) e __javascript__ (__.js__)
utilizando o [YUI Compressor] (http://developer.yahoo.com/yui/compressor/).

Minificar é o processo de remover caracteres desnecessários do código fonte, sem
modificar sua funcionalidade. Com isso, seus arquivos ficam menores, carregam
mais rapidamente, tornando seu site mais veloz.

Execute esse script apenas em ambiente de produção, preferencialmente ao fazer o
deploy automatizado da aplicação. Deve ser dessa forma porque a minificação
deixa o arquivo praticamente ilegível, e assim, imanutenível.

##Dependências

###Java

O [YUI Compressor] (http://developer.yahoo.com/yui/compressor/) é que faz a
minificação. O minify apenas roda o __YUI Compressor__ para todos os arquivos
__css__ e __javascript__ dos diretórios.
O __YUI Compressor__ vem congelado junto com este pacote. Contudo, ele é
desenvolvido em java e assim, ter o __java__ instalado é obrigatório para
executar o __minify__.


##USO

    minify DIRETÓRIOS [OPÇÕES]


###DIRETÓRIOS:

Podem ser passados vários diretórios, separados por espaço. Para cada diretório
passado como parâmetro é feita uma busca por arquivos __css__ e
__javascript__. Os arquivos encontrados são então substituídos por suas
versões minificadas.


###OPÇÕES:

    -h, --help      Mostra esta tela de ajuda e sai.
    -v, --version   Mostra a versão do programa e sai.


##EXEMPLO:

    $ ls ~/diretorio
    README.txt frontend.css base.css cidades.js

    $ minify ~/diretorio

    $ ls ~/diretorio
    README.txt base.css base-min.css cidades.js cidades-min.js up.css up-min.css

##AUTOR

 Hugo Henriques Maia Vieira <hugomaiavieira@gmail.com>

