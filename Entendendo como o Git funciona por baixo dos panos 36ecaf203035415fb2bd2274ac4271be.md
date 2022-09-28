# Entendendo como o Git funciona por baixo dos panos

## Tópicos fundamentais para entender o funcionamento do git

SHA1 ⇒ Secure Hash Algorithm

Gera um conjunto de caracteres identificador de 40 dígitos 

Identifica os arquivos de forma mais rápida, representa o estado do arquivo

## Objetos internos do Git

BLOBS ⇒ GUARDA O SHA1 DO ARQUIVO

![Untitled](Entendendo%20como%20o%20Git%20funciona%20por%20baixo%20dos%20panos%2036ecaf203035415fb2bd2274ac4271be/Untitled.png)

TREES ⇒ A ARVORE VAI MONTAR TODA A ESTRUTURA DE ONDE ESTÃO OS ARQUIVOS, PODENDO APONTAR PARA OS BLOBS(”ARQUIVOS”) E OUTRAS ARVORES. E TEM UM SHA1 DOS METADADOS DAS ÁRVORES, UMA COISA ESTÁ RELACIONADO COM OUTRA, MUDANDO UM ARQUIVO É MUDADO TODO O SHA1, DA ARVORE E DO BLOB

 

![Untitled](Entendendo%20como%20o%20Git%20funciona%20por%20baixo%20dos%20panos%2036ecaf203035415fb2bd2274ac4271be/Untitled%201.png)

COMMITS ⇒ VAI JUNTAR TUDO E DAR SENTIDO A ALTERAÇÕES E AÇÕES

APONTA PARA UMA MENSAGEM(COMMIT) E UM AUTOR, ALÉM DE TER UM TIMESTAMP, CARIMBO DE TEMPO, DA HORA DE CRIAÇÃO. OS COMMITS TAMBÉM POSSUEM UM SHA1, QUALQUER MUDANÇA VAI REFLETIR NO SHA1 DO BLOB, TREE E COMMIT

TUDO ISSO DA SENTIDO E MONTA UMA LINHA DO TEMPO DAS ALTERAÇÕES FEITAS

![Untitled](Entendendo%20como%20o%20Git%20funciona%20por%20baixo%20dos%20panos%2036ecaf203035415fb2bd2274ac4271be/Untitled%202.png)

## Chaves SSH e Tokens

SSH São chaves de confiança entre Computadores, no caso o meu com o do servidor do Github

No gitBash:

ssh-keygen -t ed25519 -C [thiagoantenor31@gmail.com](mailto:thiagoantenor31@gmail.com)