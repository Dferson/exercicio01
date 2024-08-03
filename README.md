
## Aula 02 - Básico sobre staging / commit

### Etapas:

a) No working dir, executar o comando:
```bash
echo 01 > arquivo.txt
```

b) Adicionar o arquivo no staging e conferir o status:
```bash
git add arquivo.txt
git status
```
Resultado: `arquivo.txt` adicionado ao staging.

c) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt":
```bash
git commit -m "git add example - arquivo.txt"
```
Resultado: `arquivo.txt` comitado.

d) Sobrescrever o conteúdo do arquivo.txt:
```bash
echo 02 > arquivo.txt
```
Resultado: `arquivo.txt` com o conteúdo sobrescrito para `02`.

e) Verificar o diffing no arquivo:
```bash
git diff
```
Resultado: Exibe a diferença entre o conteúdo atual e o conteúdo comitado.

f) Adicionar novamente o arquivo no staging e conferir o status:
```bash
git add arquivo.txt
git status
```
Resultado: `arquivo.txt` atualizado no staging.

g) Verificar o diffing no arquivo:
```bash
git diff --cached
```
Resultado: Exibe a diferença entre o arquivo no staging e o último commit.

h) Sobrescrever o conteúdo do arquivo.txt:
```bash
echo 03 > arquivo.txt
```
Resultado: `arquivo.txt` com o conteúdo sobrescrito para `03`.

i) Verificar o diffing no arquivo:
```bash
git diff
```
Resultado: Exibe a diferença entre o conteúdo atual e o conteúdo no staging.

j) Fazer o restore do arquivo da área de staging e verificar o status:
```bash
git restore --staged arquivo.txt
git status
```
Resultado: `arquivo.txt` removido do staging.

k) Realizar o commit do arquivo e verificar o log:
```bash
git add arquivo.txt
git commit -m "Atualizando arquivo.txt"
git log
```
Resultado: Log do commit mostrando o histórico de commits.

l) Adicionar um arquivo gitignore com o seguinte conteúdo:
```bash
echo "*.txt" > .gitignore
git add .gitignore
git commit -m "Adicionando .gitignore"
```
Resultado: `.gitignore` adicionado ao repositório, ignorando arquivos `.txt`.

m) Criar um arquivo novo.txt e verificar o status:
```bash
echo "novo conteúdo" > novo.txt
git status
```
Resultado: `novo.txt` não aparece no status, pois está sendo ignorado pelo `.gitignore`.
