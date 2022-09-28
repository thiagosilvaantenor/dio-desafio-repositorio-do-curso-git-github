# Resolvendo conflitos do GitHub

Conflito de merge ⇒ Quando um arquivo no repositório remoto está mais atualizado do que o do local, exemplo alguem coloca mais uma linha no readme, envia pro github, enquanto isso estou a modificar essa mesma linha no readme sem atualizar esse repositorio local, ao commitar o meu readme aparecerá o seguinte erro:

![Untitled](Resolvendo%20conflitos%20do%20GitHub%20bd6fadc890fc4723a47f84c6f5f453c3/Untitled.png)

Como possível resolução existe o comando:

git pull ⇒ puxar conteúdo para o repositório local

Quando usar esse comando e houver conflitos, o próprio git informará em quais arquivos estão tendo problema, e por isso ele não poderá puxar o conteúdo do repositório remoto para o local, com a exceção o arquivo conflitante

O arquivo conflitante vai estar com as seguintes marcações, comentários:

```markdown
<<<<<< HEAD

CONTEUDO DO REPOSITORIO LOCAL 

=======

CONTEUDO DO REPOSITORIO REMOTO
```

Então para resolver, basta verificar como deve ficar a versão final, fazer as modificações no arquivo conflitante, commita novamente o arquivo e empurrar(push) esse commit