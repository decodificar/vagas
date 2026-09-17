# Agente de Vagas Universal

Um agente de IA (instruções de sistema para GPT/Claude/Gemini) que atua como consultor pessoal de candidaturas: analisa vagas, calcula compatibilidade com seu perfil, monta currículos direcionados, ajuda escrever cover letters para incluir palavras chaves que as ATS utilizam para filtrar perfis. Tudo com base apenas em informações reais que você fornece, sem inventar experiência.

## O que ele faz

- **Constrói seu perfil profissional** aos poucos, sem interrogatório — a partir do que você já contou, do currículo ou do LinkedIn.
- **Analisa vagas** (link, descrição, print ou PDF) e extrai requisitos, senioridade, tecnologias, benefícios etc.
- **Calcula compatibilidade** entre seu perfil e a vaga, classificando cada requisito como atende / atende parcialmente / não atende / não informado, com uma estimativa de match em %.
- **Recomenda prioridade de candidatura** (alta, com ajustes, baixa, não recomendada), sempre explicando o motivo.
- **Gera currículo direcionado** para uma vaga específica, otimizado para leitura humana e ATS (Gupy, Greenhouse, Ashby, Workday, Lever etc.), sem keyword stuffing.
- **Escreve cover letter** ajuda com as palavras chaves na cover letter quando fizer sentido para a vaga.
- **Compara várias vagas** ao mesmo tempo e sugere uma ordem de prioridade.
- **Isola perfis diferentes** se você usar o agente para ajudar outra pessoa, não mistura experiências de pessoas diferentes.

## O que ele nunca faz

- Inventar empresas, cargos, tecnologias, certificações, idiomas ou resultados que você não informou.
- Aumentar seu nível de idioma além do que você disse.
- Prometer que você será contratado.
- Misturar informações de perfis diferentes.

Quando existe uma lacuna entre o que a vaga pede e o que você tem, o agente é transparente sobre isso e sugere como apresentar experiência transferível — sem transformar isso em uma mentira.

## Como usar

### Opção 1 — GPT customizado (ChatGPT)
1. Crie um GPT novo em [chat.openai.com/gpts/editor](https://chat.openai.com/gpts/editor).
2. Cole o conteúdo de [`instrucoes.md`](instrucoes.md) no campo de instruções.
3. Comece a conversa dizendo que quer configurar seu perfil — o agente vai conduzir o onboarding.

### Opção 2 — Projeto no Claude
1. Crie um novo Projeto no Claude.
2. Cole o conteúdo de [`instrucoes.md`](instrucoes.md) nas instruções personalizadas do projeto.
3. Envie seu currículo e/ou LinkedIn como primeiro material do projeto.

### Fluxo de uso típico
1. **Configure o perfil**: mande seu currículo, LinkedIn e conte suas preferências (cargo, senioridade, localização, modelo de trabalho).
2. **Envie uma vaga**: link, texto copiado ou print.
3. **Peça a análise completa** — o agente devolve resumo da vaga, % de compatibilidade, pontos fortes, gaps, palavras-chave e recomendação de prioridade.
4. **Peça o currículo direcionado** para aquela vaga específica, se a prioridade for boa.
5. **Peça a cover letter**, se a vaga justificar.
6. Repita para novas vagas — o agente vai lembrando do seu perfil ao longo da conversa.

## Limitações

- Precisa que você forneça as informações reais — ele não pesquisa seu histórico sozinho.
- Em conversas muito longas, pode valer a pena reforçar alguma regra específica (ex: nível de idioma) se perceber que ele está esquecendo algum detalhe.
- Score de compatibilidade é uma estimativa, não uma previsão de contratação.