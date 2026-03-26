# Awesome Agent Skills

[English](README.md) | [Português (Brasil)](README.pt-BR.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

Uma lista curada de skills, ferramentas e capacidades para agentes de codificação com IA.

---

## Sumário

- [O que são Agent Skills?](#o-que-são-agent-skills)
- [Agentes Compatíveis](#agentes-compatíveis)
- [Lista de Skills](#lista-de-skills)
- [Tutoriais e Guias Oficiais](#tutoriais-e-guias-oficiais)
- [Como usar Skills](#como-usar-skills)
- [Como criar Skills](#como-criar-skills)
- [Recursos da Comunidade](#recursos-da-comunidade)
- [Perguntas Frequentes](#perguntas-frequentes)
- [Contribuindo](#contribuindo)
- [Licença](#licença)
- [Referências](#referências)

---

## O que são Agent Skills?

Pense em **Agent Skills** como “guias de instruções” para assistentes de IA. Em vez de a IA precisar saber tudo de antemão, as skills permitem que ela aprenda novas capacidades sob demanda — como entregar uma receita pronta, em vez de fazer alguém decorar um livro inteiro.

Skills são arquivos de texto simples (chamados `SKILL.md`) que ensinam a IA a executar tarefas específicas. Quando você pede algo, a IA encontra a skill correta, lê as instruções e executa.

### Como funciona

As skills carregam em três etapas:

1. **Browse** — A IA vê a lista de skills disponíveis (só nomes e descrições curtas)
2. **Load** — Quando precisa de uma skill, a IA lê as instruções completas
3. **Use** — A IA segue as instruções e usa quaisquer arquivos auxiliares

### Por que isso importa

- **Mais rápido e leve** — A IA só carrega o que precisa, quando precisa
- **Funciona em qualquer lugar** — Crie uma skill uma vez e use em qualquer ferramenta compatível
- **Fácil de compartilhar** — Skills são arquivos que você pode copiar, baixar ou publicar no GitHub

Skills são **instruções**, não código. A IA lê como um humano leria um manual e segue os passos.

---

## Agentes Compatíveis

As plataformas abaixo têm suporte documentado para Agent Skills:

| Agente | Documentação |
|-------|---------------|
| Claude Code | [code.claude.com/docs/en/skills](https://code.claude.com/docs/en/skills) |
| Claude.ai | [support.claude.com](https://support.claude.com/en/articles/12512180-using-skills-in-claude) |
| Codex (OpenAI) | [developers.openai.com](https://developers.openai.com/codex/skills) |
| GitHub Copilot | [docs.github.com](https://docs.github.com/copilot/concepts/agents/about-agent-skills) |
| VS Code | [code.visualstudio.com](https://code.visualstudio.com/docs/copilot/customization/agent-skills) |
| OpenCode | [opencode.ai/docs](https://opencode.ai/docs) |
| Antigravity | [antigravity.google](https://antigravity.google/docs/skills) |
| Kiro | [kiro.dev](https://kiro.dev/docs/skills/) |
| Gemini CLI | [geminicli.com](https://geminicli.com/docs/cli/skills/) |

---

## Lista de Skills

### Skills Oficiais do Claude (Processamento de Documentos)

Claude oferece skills nativas para tipos comuns de documento:

| Skill | Descrição | Fonte |
|-------|-------------|--------|
| docx | Criar, editar e analisar documentos Word com controle de alterações | [anthropics/skills](https://github.com/anthropics/skills) |
| xlsx | Manipulação de planilhas: fórmulas, gráficos e transformações | [anthropics/skills](https://github.com/anthropics/skills) |
| pptx | Ler, gerar e ajustar slides, layouts e templates | [anthropics/skills](https://github.com/anthropics/skills) |
| pdf | Extrair texto, tabelas e metadados de PDFs | [anthropics/skills](https://github.com/anthropics/skills) |

### Skills Oficiais do OpenAI Codex

O Codex suporta skills em diferentes escopos:

| Escopo | Local | Uso sugerido |
|-------------|----------|---------------|
| REPO | `$CWD/.codex/skills` | Skills relevantes para uma pasta de trabalho (ex.: microserviço ou módulo) |
| REPO | `$CWD/../.codex/skills` | Skills para áreas compartilhadas em pastas pai |
| REPO | `$REPO_ROOT/.codex/skills` | Skills de raiz para todos do repositório |
| USER | `$CODEX_HOME/skills` (padrão: `~/.codex/skills`) | Skills pessoais para qualquer repositório |
| ADMIN | `/etc/codex/skills` | Scripts do SDK, automações e skills padrão administrativas |
| SYSTEM | Incluído com o Codex | Skills nativas como skill-creator e plan |

### Skills Oficiais da HuggingFace

| Skill | Descrição | Fonte |
|-------|-------------|--------|
| hf_dataset_creator | Prompts, templates e scripts para criar datasets estruturados | [huggingface/skills](https://github.com/huggingface/skills) |
| hf_model_evaluation | Instruções e utilitários para orquestrar avaliações e gerar relatórios | [huggingface/skills](https://github.com/huggingface/skills) |
| hf-llm-trainer | Skill completa de treinamento com guias, scripts e estimativas de custo | [huggingface/skills](https://github.com/huggingface/skills) |
| hf-paper-publisher | Ferramentas para publicar e gerenciar papers no Hugging Face Hub | [huggingface/skills](https://github.com/huggingface/skills) |

### Skills da Comunidade

Skills e coleções mantidas pela comunidade (verifique antes de usar):

#### Coleções de Skills

| Repositório | Descrição |
|------------|-------------|
| [anthropics/skills](https://github.com/anthropics/skills) | Coleção oficial da Anthropic (edição de documentos, análise de dados) |
| [openai/skills](https://github.com/openai/skills) | Catálogo oficial de skills do OpenAI Codex |
| [huggingface/skills](https://github.com/huggingface/skills) | Skills da HuggingFace (compatível com Claude, Codex, Gemini) |
| [skillcreatorai/Ai-Agent-Skills](https://github.com/skillcreatorai/Ai-Agent-Skills) | Coleção SkillCreator.ai com instalador CLI |
| [agentskill.sh](https://agentskill.sh) | Diretório com 44k+ skills, scanner de segurança e instalador `/learn` |
| [karanb192/awesome-claude-skills](https://github.com/karanb192/awesome-claude-skills) | Mais de 50 skills verificadas para Claude Code e Claude.ai |
| [shajith003/awesome-claude-skills](https://github.com/shajith003/awesome-claude-skills) | Skills para capacidades especializadas |
| [GuDaStudio/skills](https://github.com/GuDaStudio/skills) | Skills de colaboração multiagente |
| [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) | Integração com Pydantic AI |
| [OmidZamani/dspy-skills](https://github.com/OmidZamani/dspy-skills) | Skills para o framework DSPy |
| [hikanner/agent-skills](https://github.com/hikanner/agent-skills) | Coleção curada de Claude Agent Skills |
| [gradion-ai/freeact-skills](https://github.com/gradion-ai/freeact-skills) | Skills da biblioteca Freeact |
| [dmgrok/agent_skills_directory](https://github.com/dmgrok/agent_skills_directory) | CLI estilo npm para skills (`brew install dmgrok/tap/skills`) — agrega 177+ skills de 24 provedores |
| [gotalab/skillport](https://github.com/gotalab/skillport) | Distribuição de skills via CLI ou MCP |
| [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace) | Skills de Git, code review e testes |
| [kukapay/crypto-skills](https://github.com/kukapay/crypto-skills) | Skills de cripto, Web3 e blockchain |
| [chadboyda/agent-gtm-skills](https://github.com/chadboyda/agent-gtm-skills) | 18 skills de go-to-market: pricing, outbound, SEO, ads, retenção e operações |
| [product-on-purpose/pm-skills](https://github.com/product-on-purpose/pm-skills) | 24 skills de produto: discovery, definição, entrega e otimização |
| [sanjay3290/ai-skills](https://github.com/sanjay3290/ai-skills) | Google Workspace (Gmail, Chat, Calendar, Docs, Drive, Sheets, Slides), delegação de IA (Jules, Manus, Deep Research) e skills de banco de dados |
| [RioBot-Grind/agentfund-skill](https://github.com/RioBot-Grind/agentfund-skill) | Crowdfunding para agentes de IA na chain Base — escrow por marcos |

#### Processamento de Documentos

| Skill | Descrição |
|-------|-------------|
| [Markdown to EPUB](https://github.com/smerchek/claude-epub-skill) | Converte documentos Markdown em ebooks EPUB profissionais |

#### Desenvolvimento e Ferramentas de Código

| Skill | Descrição |
|-------|-------------|
| [aws-skills](https://github.com/zxkane/aws-skills) | Desenvolvimento AWS com melhores práticas CDK |
| [D3.js Visualization](https://github.com/chrisvoncsefalvay/claude-d3js-skill) | Gráficos D3 e visualizações interativas |
| [Playwright Automation](https://github.com/lackeyjb/playwright-skill) | Automação de navegador para testes web |
| [Specrate](https://github.com/rickygao/specrate) | Gerencie specs e mudanças com fluxo estruturado |
| [iOS Simulator](https://github.com/conorluddy/ios-simulator-skill) | Interagir com o Simulador iOS para testes |
| [Swift Concurrency Migration](https://github.com/kylehughes/the-unofficial-swift-concurrency-migration-skill) | Guia de migração para Swift Concurrency |
| [Obsidian Plugin](https://github.com/gapmiss/obsidian-plugin-skill) | Desenvolvimento de plugin para Obsidian.md |
| [Stream Coding](https://github.com/frmoretto/stream-coding) | Metodologia Stream Coding |
| [SwiftUI Skills](https://github.com/ameyalambat128/swiftui-skills) | Guia de SwiftUI e plataforma extraído do Xcode |
| [Tool Advisor](https://github.com/dragon1086/claude-skills) | Analisa prompts e recomenda ferramentas, skills e agentes ideais |
| [Vibe Testing](https://github.com/knot0-com/vibe-testing) | Stress-test de specs com raciocínio LLM antes de codar |
| [Mantra](https://mantra.gonewx.com) | Gestão de sessões de codificação com IA — salvar, restaurar e “viajar no tempo” entre sessões de Claude Code, Cursor e Windsurf |

#### Dados e Análise

| Skill | Descrição |
|-------|-------------|
| [CSV Summarizer](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill) | Analisa CSVs e gera insights com visualizações |
| [Kaggle Skill](https://github.com/shepsci/kaggle-skill) | Integração completa com Kaggle — setup de conta, relatórios de competição, download de datasets/modelos, execução de notebooks, submissões e badges |

#### Integração e Automação

| Skill | Descrição |
|-------|-------------|
| [Dev Browser](https://github.com/SawyerHood/dev-browser) | Capacidade de navegador web para agentes |
| [Vectorize MCP Worker](https://github.com/dannwaneri/vectorize-mcp-worker) | Padrões de servidor MCP “edge-native” para RAG em produção |
| [Agent Manager](https://github.com/fractalmind-ai/agent-manager-skill) | Gerencie agentes CLI locais via tmux (start/stop/monitor/assign + cron) |
| [HOL Claude Skills](https://github.com/hashgraph-online/hol-claude-skills) | Descoberta de agentes via Registry Broker - /hol-search, /hol-resolve, /hol-chat |
| [Sheets CLI](https://github.com/gmickel/sheets-cli) | Automação CLI do Google Sheets |
| [Notification Skill](https://github.com/caopulan/Notification-Skill) | Envio de notificações para fluxos de agentes |
| [Spotify Skill](https://github.com/fabioc-aloha/spotify-skill) | Integração com a API do Spotify |
| [AgentStore](https://github.com/techgangboss/agentstore) | Marketplace open-source de plugins com pagamentos USDC sem gas, instalação via CLI e API de publicação de 3 campos |
| [Transloadit Skills](https://github.com/transloadit/skills) | Processamento de mídia: encoding de vídeo, manipulação de imagens, OCR e 86+ robots |
| [commune](https://github.com/shanjairaj7/commune-skill) | Inbox nativa para agentes — endereço permanente @commune.ai com envio/recebimento, busca semântica, triagem e webhooks |

#### Colaboração e Gestão de Projetos

| Skill | Descrição |
|-------|-------------|
| [git-pushing](https://github.com/mhattingpete/claude-skills-marketplace) | Automatiza operações git e interações com repositórios |
| [review-implementing](https://github.com/mhattingpete/claude-skills-marketplace) | Avalia planos de implementação de código |
| [test-fixing](https://github.com/mhattingpete/claude-skills-marketplace) | Detecta testes falhando e propõe correções |

#### Segurança e Sistemas

| Skill | Descrição |
|-------|-------------|
| [computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace) | Análise e investigação de forense digital |
| [safe-encryption-skill](https://github.com/grittygrease/safe-encryption-skill) | Alternativa moderna ao GPG/PGP com suporte pós-quântico, autenticação composable e comunicação agente-a-agente |
| [Threat Hunting](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) | Caça a ameaças usando regras Sigma |
| [Vincent Wallet](https://github.com/HeyVincent-ai/agent-skills/tree/main/wallet) | Carteira EVM segura para agentes — transferências, swaps e transações |
| [Vincent Polymarket](https://github.com/HeyVincent-ai/agent-skills/tree/main/polymarket) | Trading em mercados de previsão Polymarket para agentes |
| [Agent OS Governance](https://github.com/imran-siddique/agent-os) | Governança no nível de kernel para agentes — aplicação determinística de políticas, compliance e auditoria |

#### Avançado e Pesquisa

| Skill | Descrição |
|-------|-------------|
| [Context Engineering](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering) | Técnicas de engenharia de contexto |
| [Pomodoro System Skill](https://github.com/jakedahn/pomodoro) | Padrão de Skill de Sistema (skills que lembram e melhoram) |
| [Mind Cloning](https://github.com/yzfly/Mind-Cloning-Engineering) | Clonagem mental com skills LLM |

---

## Tutoriais e Guias Oficiais

### Claude e Anthropic
- [Usando skills no Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude) - Guia oficial de início rápido
- [Como criar skills personalizadas](https://support.claude.com/en/articles/12512198-creating-custom-skills) - Passo a passo de autoria
- [Documentação de Skills do Claude Code](https://code.claude.com/docs/en/skills) - Referência oficial

### GitHub Copilot
- [Sobre Agent Skills](https://docs.github.com/copilot/concepts/agents/about-agent-skills) - Documentação oficial
- [VS Code Agent Skills](https://code.visualstudio.com/docs/copilot/customization/agent-skills) - Integração no VS Code

### Model Context Protocol (MCP)
- [Documentação oficial do MCP](https://modelcontextprotocol.io/) - O padrão aberto
- [Construa seu primeiro servidor MCP](https://modelcontextprotocol.io/docs/first-server) - Guia Python/TypeScript
- [Exemplos de servidor MCP](https://github.com/modelcontextprotocol/servers) - Implementações oficiais

---

## Como usar Skills

### Usando Skills no Claude.ai
1. Clique no ícone de skills na interface do chat.
2. Adicione skills do marketplace ou envie skills personalizadas.
3. Claude ativa automaticamente as skills relevantes com base na tarefa.

### Usando Skills no Google Antigravity

O Antigravity suporta dois tipos de skills:

*   **Workspace Skills**: skills específicas do projeto em `/.agent/skills/`
*   **Global Skills**: skills globais do usuário em `~/.gemini/antigravity/skills`

Para mais detalhes, veja a [documentação oficial](https://antigravity.google/docs/skills).

### Usando Skills no Claude Code

Coloque a skill no diretório de configuração:

```bash
mkdir -p ~/.claude/skills/
cp -r skill-name ~/.claude/skills/
```

A skill carrega automaticamente e ativa quando for relevante.

### Usando Skills no OpenCode

Instale o OpenCode globalmente para ficar disponível em qualquer projeto:

```bash
curl -fsSL https://opencode.ai/install | bash
# ou
npm i -g opencode-ai@latest
brew install anomalyco/tap/opencode
```

Depois de instalar, você pode rodar `opencode` de qualquer workspace. Consulte a documentação para configurar providers e modelos.

**Caminhos de descoberta de skills:**

- Projeto: `.opencode/skills/<name>/SKILL.md`
- Global: `~/.config/opencode/skills/<name>/SKILL.md`
- Também compatível: `.claude/skills/<name>/SKILL.md`, `~/.claude/skills/<name>/SKILL.md`, `.agents/skills/<name>/SKILL.md`, `~/.agents/skills/<name>/SKILL.md`

### Usando Skills no Codex

**Criar uma skill:**

Use a skill embutida `$skill-creator` no Codex. Descreva o que você quer e o Codex cria a estrutura para você.

Se você instalar `$create-plan` (experimental) com `$skill-installer create-plan`, o Codex fará um plano antes de escrever arquivos.

Você também pode criar manualmente criando uma pasta com `SKILL.md`:

```markdown
---
name: skill-name
description: Descrição que ajuda o Codex a selecionar a skill
metadata:
  short-description: Descrição opcional para o usuário
---

Instruções da skill para o agente Codex seguir ao usar esta skill.
```

**Instalar novas skills:**

Baixe skills do GitHub usando `$skill-installer`:

```bash
$skill-installer linear
```

Você também pode pedir para o instalador baixar skills de outros repositórios. Depois de instalar, reinicie o Codex para carregar as novas skills.

### Usando Skills no VS Code

Skills ficam em diretórios com um arquivo `SKILL.md`. O VS Code suporta dois locais:

- `.github/skills/` — Local recomendado para novas skills
- `.claude/skills/` — Local legado, ainda suportado

**Criar uma skill:**

1. Crie o diretório `.github/skills` no workspace
2. Crie um subdiretório para a sua skill (ex.: `.github/skills/webapp-testing`)
3. Crie um arquivo `SKILL.md` com a estrutura abaixo

```markdown
---
name: skill-name
description: Descrição do que a skill faz e quando usar
---

# Instruções da Skill

Suas instruções detalhadas, exemplos e diretrizes vão aqui...
```

### Usando Skills no Copilot CLI

**Adicionando skills ao repositório:**

1. Crie um diretório `.github/skills` (skills em `.claude/skills` também são suportadas)
2. Crie um subdiretório para sua skill (ex.: `.github/skills/webapp-testing`)
3. Crie um arquivo `SKILL.md` com as instruções da sua skill

**Estrutura do SKILL.md:**

- `name` (obrigatório): identificador único em minúsculas com hífens
- `description` (obrigatório): o que a skill faz e quando o Copilot deve usá-la
- `license` (opcional): licença que se aplica à skill
- Corpo em Markdown com instruções, exemplos e diretrizes

**Exemplo de SKILL.md:**

```markdown
---
name: github-actions-failure-debugging
description: Guia para depurar workflows do GitHub Actions que falharam.
---

Para depurar workflows com falha:

1. Use `list_workflow_runs` para encontrar execuções recentes
2. Use `summarize_job_log_failures` para obter um resumo dos jobs com falha
3. Use `get_job_logs` para logs detalhados se necessário
4. Tente reproduzir a falha no seu ambiente
5. Corrija a build que falhou
```

Quando realiza tarefas, o Copilot decide quando usar skills com base no seu prompt e na descrição da skill. O arquivo `SKILL.md` é injetado no contexto do agente.

### Usando Servidores MCP (Claude Desktop)

Edite seu arquivo de configuração:

- **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

Exemplo de configuração:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/Users/username/Desktop"
      ]
    }
  }
}
```

---

## Como criar Skills

Skills são pacotes de instruções que dizem ao agente como executar tarefas. Não são código executável por padrão.

### Estrutura de uma Skill

```
skill-name/
├── SKILL.md          # Obrigatório: instruções e metadados
├── scripts/          # Opcional: scripts auxiliares
├── templates/        # Opcional: templates de documentos
└── resources/        # Opcional: arquivos de referência
```

### Template básico de SKILL.md

```markdown
---
name: my-skill-name
description: Uma descrição clara do que a skill faz.
---

# Nome da Minha Skill

Descrição detalhada do propósito da skill.

## Quando usar esta skill

- Caso de uso 1
- Caso de uso 2

## Instruções

[Instruções detalhadas para o agente seguir]

## Exemplos

[Exemplos reais]
```

### Exemplo de servidor MCP (Python)

Para skills que precisam acessar dados externos, você pode criar um servidor MCP:

```bash
pip install fastmcp
```

server.py:

```python
from fastmcp import FastMCP

mcp = FastMCP("My Server")

@mcp.tool()
def hello_world(name: str = "World") -> str:
    """Uma ferramenta simples que diz olá."""
    return f"Hello, {name}!"

if __name__ == "__main__":
    mcp.run()
```

---

## Recursos da Comunidade

### Ferramentas LangChain
- [Google Search](https://python.langchain.com/docs/integrations/tools/google_search/) - Wrapper do SerpApi
- [Wikipedia](https://python.langchain.com/docs/integrations/tools/wikipedia/) - Busca resumos na Wikipedia
- [Python REPL](https://python.langchain.com/docs/integrations/tools/python/) - Executa código Python
- [Guia de Ferramentas Customizadas](https://python.langchain.com/docs/how_to/custom_tools/) - Como usar o decorator `@tool`

### Artigos e Pesquisa
- [I found 50 companies accidentally breaking HIPAA with ChatGPT](https://dev.to/dannwaneri/i-found-50-companies-accidentally-breaking-hipaa-with-chatgpt-1olc) - Análise de riscos de privacidade em IA
- [I built a Production RAG System for $5/month](https://dev.to/dannwaneri/i-built-a-production-rag-system-for-5month-most-alternatives-cost-100-200-21hj) - Guia de otimização de custos para arquiteturas RAG

---

## Perguntas Frequentes

### O que são Agent Skills?

Agent Skills são arquivos de instruções que ensinam assistentes de IA a executar tarefas específicas. Elas carregam apenas quando necessárias, mantendo a IA rápida e focada.

### Qual a diferença entre Agent Skills e fine-tuning?

Fine-tuning muda permanentemente o comportamento da IA (caro e difícil de atualizar). Agent Skills são só arquivos de texto: você pode atualizar, trocar ou compartilhar sem mexer no modelo.

### Qual a diferença entre Agent Skills e MCP?

Eles têm papéis diferentes e funcionam bem juntos:

- **Agent Skills** = ensinam *como* fazer algo (workflow e boas práticas)
- **MCP** = ajudam a IA *acessar* coisas (APIs, bancos de dados e ferramentas externas)

### Quais ferramentas suportam Agent Skills?

Atualmente suportadas: **Claude** (Claude.ai e Claude Code), **GitHub Copilot**, **VS Code**, **OpenCode**, **Codex** (OpenAI), **Antigravity** (Google), **Gemini CLI** e **Kiro**. A lista cresce à medida que mais ferramentas adotam o padrão.

### Agent Skills executam código?

Não. Skills são somente instruções. Se você precisa executar código, use algo como servidores MCP junto com skills.

### Como criar minha primeira Agent Skill?

1. Crie um `SKILL.md` com nome e descrição no topo
2. Escreva instruções claras e passo a passo
3. Coloque o arquivo em `.github/skills/` ou `.claude/skills/`
4. Teste a skill

Guia completo: [Como criar skills personalizadas](https://support.claude.com/en/articles/12512198-creating-custom-skills)

---

## Contribuindo

Contribuições são bem-vindas. Veja **[CONTRIBUTING.md](CONTRIBUTING.md)** para o guia completo.

Resumo rápido:

- Siga o template de skill
- Forneça instruções claras e acionáveis
- Inclua exemplos funcionando quando possível
- Documente trade-offs e possíveis problemas
- Mantenha `SKILL.md` com menos de 500 linhas para melhor performance
- Verifique se a skill realmente existe antes de adicionar

---

## Licença

MIT License — veja o arquivo LICENSE para detalhes.

---

## Referências

Os princípios destas skills vêm de pesquisa e experiência em produção em laboratórios e frameworks líderes.

- [Anthropic: Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [Anthropic: Creating custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Claude Code Skills Documentation](https://code.claude.com/docs/en/skills)
- [GitHub Copilot: About Agent Skills](https://docs.github.com/copilot/concepts/agents/about-agent-skills)
- [Model Context Protocol Documentation](https://modelcontextprotocol.io/)
