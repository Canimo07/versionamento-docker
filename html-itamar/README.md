# Versionamento Docker - Aula Web

## Sobre o projeto

Esse projeto é sobre criar imagens Docker que servem uma página web simples. Vou controlar as versões dessas imagens conforme faço mudanças no conteúdo.

---

## Minhas versões

### Versão 0.2

Essa foi a imagem base inicial, só pra teste mesmo. Não tem nada específico sobre o Messi ainda.

### Versão 0.3

Aqui eu atualizei o conteúdo pra falar um pouco sobre o Messi: começo da carreira e as conquistas dele.

### Versão 0.4

Nessa versão, eu fiz uma página falando sobre os filhos do Messi e as expectativas em relação ao futebol. Também dei uma personalizada no CSS pra deixar o site mais bonito.

---

## Como eu rodo a imagem

```bash
docker pull monca07/aula-web-docker:0.4
docker run -p 80:80 monca07/aula-web-docker:0.4
```

Depois é só abrir o navegador no endereço http://localhost pra ver o site funcionando.

---

## Como eu construo e versiono a imagem

1. Faço as alterações nos arquivos `index.html` e `style.css` no meu computador.
2. No terminal, rodo os comandos:

```bash
docker build -t monca07/aula-web-docker:0.4 .
docker push monca07/aula-web-docker:0.4
```

3. Quando quero criar uma nova versão, uso:

```bash
docker tag monca07/aula-web-docker:0.4 monca07/aula-web-docker:0.5
docker push monca07/aula-web-docker:0.5
```

---

## Por que versionar?

Assim eu consigo manter o histórico das mudanças, testar diferentes versões e, se precisar, voltar pra uma versão antiga sem perder nada.

