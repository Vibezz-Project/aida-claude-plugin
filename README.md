# AIDA Platform para Claude

A **AIDA Platform** conecta o Claude à plataforma de inteligência de mercado de cinema da Vibezz. Com ele, você faz perguntas em linguagem natural e o Claude responde com análises da AIDA.

*English summary below.*

## O que o plugin faz

O plugin adiciona um conector MCP remoto (`aida`) que dá acesso às análises da AIDA:

- **Resultado de mercado:** bilheteria e público por CineSemana, filme, exibidor, rede, cidade e estado, com comparações entre períodos.
- **Programação (showtimes):** sessões programadas por cinema e filme.
- **Pré-venda:** acompanhamento e ritmo (pacing) de pré-venda de lançamentos.
- **Fancast:** previsões de público, histórico, engajamento e backtests.
- **Auditoria de ocupação:** auditorias pontuais de mapas de assentos e de ocupação histórica.
- **Catálogo:** busca e detalhes de filmes e cinemas.

A AIDA entrega análises, rankings e agregações. Ela não exporta bases brutas nem dados em nível de registro.

## Requisitos

- Uma **conta AIDA ativa**, com acesso liberado pela Vibezz. Sem conta, o conector não autentica e nenhuma ferramenta funciona.
- Os módulos disponíveis dependem das permissões da sua conta. Pergunte ao Claude *"o que posso fazer com o AIDA?"* para ver os seus.

## Como usar

1. Adicione o plugin **AIDA Platform** pelo diretório no claude.ai.
2. Abra a aba **Conectores** do plugin, selecione **aida** e entre com a sua conta AIDA.
3. Em uma conversa, ative o conector e faça uma pergunta, por exemplo: *"Qual foi o resultado de mercado desta CineSemana no Brasil?"*

No Claude Code, também é possível instalar direto deste repositório:

```
/plugin install vibezz-aida --marketplace Vibezz-Project/aida-claude-plugin
```

## Dados e privacidade

- O plugin não contém código executável, tokens nem credenciais. Ele só aponta para o servidor `https://aida.vibezz.com/mcp`.
- O login é feito por OAuth no próprio serviço da AIDA.
- As perguntas que exigem ferramentas da AIDA e os parâmetros dessas consultas (filmes, cinemas, datas e filtros) são enviados ao servidor da AIDA, que aplica as permissões, cotas e regras de auditoria da sua conta.
- Nenhum dado é enviado a outros serviços além do servidor da AIDA.

## Suporte e links

- Suporte: https://aida.vibezz.com/support
- Política de privacidade (Privacy): https://aida.vibezz.com/privacy
- Termos de uso: https://aida.vibezz.com/terms
- Site da Vibezz: https://vibezz.com/

---

## English summary

**AIDA Platform** connects Claude to Vibezz's cinema market intelligence platform. It adds a remote MCP connector for box office results, showtimes, pre-sales pacing, Fancast audience forecasts, and seat occupancy audits across Latin American markets. The platform returns aggregated analyses only, never raw record-level data. You need an active AIDA account: sign in through OAuth on the plugin's Connectors tab. The plugin ships no executable code or credentials, and data is sent only to `https://aida.vibezz.com/mcp`.
