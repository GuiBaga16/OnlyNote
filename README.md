# Tecnico Informatica: Manuteção de Software.

-Nesta cadeira pretendo aprender como manter um software sobre git e github;

-Vou colocar neste repositório tudo que pode agregar para meu aprendizado profissional;

-Pretendo anotar neste Readme comandos importantes também.
:)

<hr>

# Tutorial: Configurar um Domínio Personalizado no GitHub Pages

## Pré-requisitos:
- Um repositório no GitHub com seu site.
- A publicação do site já configurada via GitHub Pages.
- Acesso ao painel de controle do seu domínio.

---

## Passo 1: Configurar GitHub Pages
1. Acesse o repositório no GitHub.
2. Vá em **Settings > Pages**.
3. Certifique-se de que a branch correta (geralmente `main`) está selecionada em **Source**.
4. Clique em **Save** (se necessário) para ativar o GitHub Pages.

---

## Passo 2: Adicionar o Domínio Personalizado
1. Ainda em **Settings > Pages**, encontre a seção **Custom domain**.
2. Insira o domínio adquirido, como `bagadev.com`.
3. Clique em **Save**.

⚠️ Após salvar, o GitHub criará um arquivo chamado `CNAME` no seu repositório com o nome do domínio.

---

## Passo 3: Configurar o DNS no Painel do Domínio
1. Acesse o painel de controle do seu domínio.
2. Vá até a seção de gerenciamento de **DNS**.
3. Adicione as seguintes entradas de **CNAME** e **A**:

### CNAME
- **Host**: `www`  
- **Valor**: `your-github-username.github.io`  
- **TTL**: Automático ou Padrão.

### A (para o domínio sem "www")
Adicione as seguintes entradas de tipo **A**:
- **Host**: `@`  
- **Valores**:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`  
- **TTL**: Automático ou Padrão.

---

## Passo 4: Esperar a Propagação do DNS
- Pode levar de **30 minutos a 48 horas** para o domínio apontar corretamente para o site.

---

## Passo 5: Testar o Domínio
1. Acesse o domínio personalizado (`bagadev.com`) e veja se está funcionando.
2. Certifique-se de que o redirecionamento de `www` para o domínio raiz (ou vice-versa) funciona corretamente.

💡 **Dica**: Ative o **HTTPS** na página de configuração do GitHub Pages para garantir segurança.

---

Com isso, seu domínio estará funcionando no GitHub Pages!

