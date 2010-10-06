#Minify

Minifica arquivos arquivos _css_ (_.css_) e _javascript_ (_.js_) utilizando o
[YUI Compressor](http://developer.yahoo.com/yui/compressor/).

Minificar é o processo de remover caracteres desnecessários do código fonte, sem
modificar sua funcionalidade. Com isso, seus arquivos ficam menores, carregam
mais rapidamente, tornando seu site mais veloz.

Execute esse script apenas em ambiente de produção, preferencialmente ao fazer o
deploy automatizado da aplicação. Deve ser dessa forma porque a minificação
deixa o arquivo praticamente ilegível, e assim, imanutenível.

##Dependências

###Java

O [YUI Compressor](http://developer.yahoo.com/yui/compressor/) é que faz a
minificação. O minify apenas roda o _YUI Compressor_ para todos os arquivos
_css_ e _javascript_ dos diretórios.

O _YUI Compressor_ vem congelado junto com este pacote. Contudo, ele é
desenvolvido em _java_. Dessa forma, ter o _java_ instalado é obrigatório para
executar o _minify_.


##USO

    minify DIRETÓRIOS [OPÇÕES]


###DIRETÓRIOS:

Podem ser passados vários diretórios, separados por espaço. Para cada diretório
passado como parâmetro é feita uma busca por arquivos _css_ e _javascript_. Os
arquivos encontrados são então substituídos por suas versões minificadas.


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

