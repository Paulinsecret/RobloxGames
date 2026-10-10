# Guia de Configuração: Desenvolvimento Roblox (Rojo + Git)

Olá! Se você está lendo isso, nós estamos configurando nosso ambiente profissional para desenvolvermos juntos no Roblox usando **Rojo** e **Git**.

Em vez de usarmos o *Team Create* para editar os scripts (o que causa perda de código e conflitos), nós vamos usar a abordagem de estúdios profissionais:
- **Mapas e Modelos (3D):** Continuamos fazendo via Roblox Studio / Team Create.
- **Códigos e Scripts:** Vamos escrever no computador e versionar via Git/GitHub. O Rojo sincroniza isso para o Roblox Studio.

---

## Passo a Passo para você (Humano)
1. **Baixe o repositório:** Peça para eu te passar o link do nosso GitHub e faça o `git clone` na sua máquina (ex: na pasta `c:\Projects\Roblox`).
2. **Instale o Plugin do Rojo:** Abra o seu Roblox Studio, vá em "Plugins", "Manage Plugins" e instale o Plugin oficial do **Rojo**.
3. **Passe o contexto para a sua IA:** Copie o bloco de texto abaixo e envie para o seu ChatGPT, Claude ou assistente de IA. Isso vai deixá-lo no mesmo nível de conhecimento que o meu, e ele mesmo fará a instalação técnica para você!

---

## 🤖 COPIE E COLE O TEXTO ABAIXO PARA O SEU ASSISTENTE DE IA 🤖

```text
Olá! A partir de agora você atuará como meu Assistente Sênior de Desenvolvimento Roblox. Eu estou desenvolvendo um jogo em equipe com um amigo e nós estamos utilizando o fluxo de trabalho profissional com **Rojo** e **Git**.

**O nosso Contexto e Regras de Trabalho:**
1. O nosso mapa e UI são feitos no Team Create do Roblox Studio, mas **TODO O CÓDIGO** do jogo é gerenciado localmente via Git para evitar conflitos.
2. A estrutura do nosso projeto utiliza o Rojo. Nós temos um arquivo `default.project.json` que mapeia pastas como `src/ServerScriptService` diretamente para dentro do jogo.
3. **A sua missão (como IA):** Você não precisa me dar blocos de código para eu copiar e colar. Sempre que eu pedir para criarmos um sistema novo, você deve gerar o arquivo `.lua` localmente na minha pasta do projeto. O Rojo vai se encarregar de sincronizar para o meu Roblox Studio automaticamente.

**A sua primeira tarefa de hoje:**
Verifique o meu sistema operacional. Eu preciso que você instale o **Rojo CLI** no meu terminal (pode usar ferramentas como Aftman, Foreman ou npm se eu tiver instalado, ou baixar direto). Verifique também se eu já tenho o Git configurado. Me guie passo a passo para conectarmos o meu Rojo ao meu Roblox Studio. Confirme que entendeu o nosso fluxo de trabalho e aguarde meu próximo comando!
```
