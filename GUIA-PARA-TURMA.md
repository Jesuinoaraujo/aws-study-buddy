# Guia de instalação e teste — AWS Study Buddy

Este guia explica como instalar e testar o AWS Study Buddy no seu próprio computador. Não é necessário saber Git nem usar comandos no terminal.

## O que você precisa

- Um computador compatível com o [Kiro IDE](https://kiro.dev/downloads/).
- Uma conta própria do Kiro. O Kiro tem um plano gratuito, sujeito a limites de uso e disponibilidade de modelos. Consulte os [planos atuais](https://kiro.dev/pricing/).
- Conexão com a internet.
- O `uv`, necessário para iniciar o servidor que consulta a documentação pública da AWS. As instruções oficiais de instalação estão em [Instalar o uv](https://docs.astral.sh/uv/getting-started/installation/).

Não é necessária uma conta AWS, uma chave de API da AWS ou uma placa de vídeo dedicada. O Kiro precisa estar instalado no computador, e o servidor MCP da documentação também é iniciado localmente; o acesso ao modelo depende da sua conta e dos limites vigentes do Kiro. O uso pode variar conforme o computador e a conexão.

## Instalação recomendada: pelo Kiro, sem Git

1. Instale e abra o [Kiro IDE](https://kiro.dev/downloads/).
2. Entre no Kiro com sua própria conta.
3. Instale o `uv` seguindo o guia oficial indicado acima. Feche e abra o Kiro novamente depois da instalação do `uv`.
4. No Kiro, abra o painel **Powers**.
5. Selecione **Add power from GitHub URL**.
6. Cole o endereço do projeto:

   `https://github.com/Jesuinoaraujo/aws-study-buddy`

7. Confirme a instalação do Power, se o Kiro pedir.
8. Abra uma pasta de trabalho no Kiro. Se não tiver uma, crie uma pasta vazia chamada `aws-estudos` e abra-a.

Não precisa clicar em **Fork**, instalar Git ou copiar o repositório para usar essa opção. O Kiro baixa o Power público diretamente do GitHub.

## Alternativa: baixar ZIP, também sem Git

Use esta opção se a instalação direta pelo Kiro não estiver disponível:

1. Abra o [repositório AWS Study Buddy](https://github.com/Jesuinoaraujo/aws-study-buddy).
2. Clique em **Code** e depois em **Download ZIP**.
3. Localize o ZIP baixado e extraia-o. No Windows, normalmente basta clicar com o botão direito e escolher **Extrair Tudo**.
4. No Kiro, abra o painel **Powers** e selecione **Add power from Local Path**.
5. Escolha a pasta extraída que contém o arquivo `POWER.md` diretamente. Não selecione o arquivo ZIP nem uma pasta acima ou abaixo dela.
6. Abra uma pasta de trabalho no Kiro. Se necessário, crie e abra uma pasta vazia para os estudos.

## Usar no VS Code com a extensão Google Antigravity

Esta opção usa a extensão oficial **Google Antigravity para VS Code**. O Antigravity não instala este repositório como um Power do Kiro: você abre os arquivos do projeto no VS Code, configura o servidor MCP e pede ao agente que siga as instruções do Study Buddy. A experiência pode não ser idêntica à do Kiro.

### Requisitos

- [Visual Studio Code 1.90 ou superior](https://code.visualstudio.com/).
- Uma conta Google com acesso ao Antigravity (incluindo o plano gratuito, conforme disponibilidade e limites atuais).
- `uv` instalado, conforme as instruções em [Instalar o uv](https://docs.astral.sh/uv/getting-started/installation/).
- Conexão com a internet.

Consulte os [requisitos oficiais da extensão Antigravity para VS Code](https://antigravity.google/docs/ide/extensions/vscode) e os [planos atuais do Antigravity](https://antigravity.google/).

### Instalar a extensão e abrir o projeto

1. Baixe e instale o [Visual Studio Code](https://code.visualstudio.com/), se ainda não o tiver.
2. No VS Code, abra **Extensions** (`Ctrl+Shift+X` no Windows/Linux ou `Cmd+Shift+X` no macOS).
3. Procure **Google Antigravity**, confirme que o publicador é **Google** e instale a extensão.
4. Clique no ícone do Antigravity na barra lateral e entre com sua própria conta Google.
5. Baixe o [ZIP do repositório](https://github.com/Jesuinoaraujo/aws-study-buddy), extraia-o e, no VS Code, escolha **File > Open Folder**. Abra a pasta que contém `POWER.md` e a pasta `steering`.

### Configurar o servidor de documentação (MCP)

O Antigravity precisa do servidor MCP para consultar a documentação pública da AWS. Na configuração MCP do Antigravity, abra ou crie o arquivo `mcp_config.json` e adicione esta entrada dentro de `mcpServers`:

```json
{
  "mcpServers": {
    "awslabs.aws-documentation-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.aws-documentation-mcp-server@latest"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR",
        "AWS_DOCUMENTATION_PARTITION": "aws"
      }
    }
  }
}
```

Se `mcp_config.json` já tiver outros servidores, preserve-os e acrescente somente a entrada `awslabs.aws-documentation-mcp-server` ao objeto `mcpServers`; não substitua o arquivo inteiro. Use a opção de configuração MCP do Antigravity para abrir ou localizar esse arquivo — o caminho depende do sistema e da versão. Salve a configuração e reinicie ou reconecte o servidor. A referência oficial está em [Configurar servidores MCP no Antigravity](https://antigravity.google/docs/mcp).

Esse servidor consulta documentação pública e não exige conta AWS ou chave de API da AWS. Não coloque credenciais no arquivo.

### Pedir ao Antigravity para usar o Study Buddy

O formato de Power e os arquivos `steering/` foram escritos para o Kiro. Para orientar o Antigravity, cole este pedido na conversa:

```text
Quero usar este repositório como material de estudo para a AWS Certified Cloud
Practitioner (CLF-C02). Antes de começar, leia POWER.md e as instruções
relevantes em steering/global-instructions.md, steering/study.md e
steering/exam-simulator.md. Use o servidor MCP de documentação da AWS
configurado para verificar informações oficiais. Não invente funcionalidades.
Comece um simulado de 3 questões de prática, uma questão por vez, e siga o
fluxo descrito nas instruções do simulador.
```

Se o agente não conseguir consultar a documentação, confirme nas configurações MCP se o servidor está conectado e se `uv` está instalado. Os nomes de menus podem variar com a versão da extensão.

## Faça um teste rápido

Na conversa do Kiro, envie:

```text
Estou estudando para a certificação AWS Certified Cloud Practitioner (CLF-C02).
Ajude-me a confirmar meu contexto de prova e depois explique o Amazon S3
com base na documentação oficial da AWS.
```

Responda às perguntas de configuração do exame. Depois, teste o simulador com um conjunto pequeno:

```text
#exam-simulator Faça um simulado de 3 questões para CLF-C02, uma questão por vez.
```

O Study Buddy apresenta as questões uma por vez. Siga as instruções da conversa para iniciar, responder e avançar. A quantidade de questões é uma escolha de prática; não representa necessariamente o tamanho do exame oficial.

## Se algo não funcionar

- **O Kiro não encontra ou não inicia o servidor de documentação:** confirme que o `uv` foi instalado, que há conexão com a internet e reinicie o Kiro.
- **O Power não aparece:** confirme que instalou o repositório correto e abra uma pasta de trabalho no Kiro.
- **A instalação por GitHub falha:** tente a opção **Download ZIP** e **Add power from Local Path**.
- **A conta gratuita atingiu um limite:** consulte os [planos e limites atuais do Kiro](https://kiro.dev/pricing/). O projeto não fornece créditos nem acesso a modelos.
- **O computador está lento:** feche aplicativos que não estiver usando e comece com poucas questões. O Kiro e o servidor MCP rodam no computador, então o desempenho pode variar conforme a máquina.

## Compartilhamento e custos

O repositório e o servidor MCP de documentação da AWS não exigem chave de API da AWS. Cada pessoa precisa usar a própria conta do Kiro; os créditos, limites e eventuais custos do modelo são individuais e seguem os termos atuais do Kiro. Verifique os [planos oficiais](https://kiro.dev/pricing/) antes de usar.

As questões geradas são material de prática e não são questões oficiais nem uma garantia de aprovação. Para estudar, consulte também o guia oficial da certificação e a documentação da AWS.
