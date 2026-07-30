# 🛡️ Fundamentos de Cibersegurança para Laboratórios Práticos com NotebookLM

> Projeto desenvolvido como parte do desafio **"Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM"** da DIO (Digital Innovation One).

![DIO](https://img.shields.io/badge/DIO-Project-blue)
![NotebookLM](https://img.shields.io/badge/NotebookLM-Google-orange)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Learning-green)
![Markdown](https://img.shields.io/badge/Markdown-README-black)
![Status](https://img.shields.io/badge/Status-Concluído-success)

## 📖 Sobre o Projeto

Este projeto tem como objetivo explorar o uso do **NotebookLM** como ferramenta de aprendizagem ativa na área de **Cibersegurança**. Em vez de utilizar a Inteligência Artificial apenas para gerar respostas prontas, a proposta foi construir um processo estruturado de estudo, utilizando fontes oficiais, engenharia de prompts e documentação do aprendizado.

O tema escolhido foi **Fundamentos de Cibersegurança para Laboratórios Práticos**, por ser uma área de grande relevância para profissionais de Tecnologia da Informação e por fornecer uma base sólida para estudos futuros em segurança ofensiva, segurança defensiva e infraestrutura.

---

<p align="center">
  <img src="imagens/notebooklm-overview.png" width="850">
</p>

## 📑 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Objetivos](#-objetivos)
- [Curadoria das Fontes](#-curadoria-das-fontes)
- [Estratégia de Aprendizagem](#-estratégia-de-aprendizagem)
- [Engenharia de Prompts](#-engenharia-de-prompts)
- [Cicatrizes (Troubleshooting)](#️-cicatrizes-troubleshooting)
- [Miniguia de Estudos](#-miniguia-de-estudos)
- [Glossário](#-glossário)
- [Prompts Reutilizáveis](#-prompts-reutilizáveis)
- [Lições Aprendidas](#-lições-aprendidas)
- [Conclusão](#-conclusão)
- [Próximos Passos](#-próximos-passos)
- [Autor](#-autor)

---

## 🎯 Objetivos

### Objetivo Geral

Construir um caderno temático utilizando o NotebookLM para organizar, compreender e revisar conceitos fundamentais de cibersegurança aplicados à criação de laboratórios práticos.

### Objetivos Específicos

- compreender os princípios fundamentais da segurança da informação;
- identificar ameaças, vulnerabilidades e mecanismos de proteção;
- aprender a utilizar fontes técnicas oficiais como base de estudo;
- experimentar diferentes estratégias de prompts no NotebookLM;
- documentar os resultados obtidos durante o processo de aprendizagem;
- produzir um miniguia reutilizável para estudos futuros.

---

## 📚 Curadoria das Fontes

Foram selecionadas cinco fontes oficiais e amplamente reconhecidas na área de Segurança da Informação.

| Fonte | Link | Objetivo | Justificativa | Contribuição para o NotebookLM |
|---|---|---|---|---|
| OWASP Top 10 | [owasp.org/www-project-top-ten](https://owasp.org/www-project-top-ten/) | Estudar as principais vulnerabilidades em aplicações web | Principal referência mundial sobre riscos de segurança em aplicações | Permitiu comparar riscos comuns em aplicações web |
| OWASP Web Security Testing Guide (WSTG) | [owasp.org/www-project-web-security-testing-guide](https://owasp.org/www-project-web-security-testing-guide/) | Compreender metodologias de testes de segurança | Complementa o Top 10 com procedimentos práticos | Forneceu metodologia prática para validação de segurança |
| NIST Cybersecurity Framework (CSF 2.0) | [nist.gov/cyberframework](https://www.nist.gov/cyberframework) | Estudar boas práticas e governança em segurança | Framework utilizado internacionalmente | Relacionou conceitos técnicos com gestão de segurança |
| Documentação Oficial do Nmap | [nmap.org/book/man.html](https://nmap.org/book/man.html) | Aprender reconhecimento de redes | Referência oficial da ferramenta | Serviu de base para estudos sobre mapeamento de redes |
| Wireshark User's Guide | [wireshark.org/docs/wsug_html_chunked](https://www.wireshark.org/docs/wsug_html_chunked/) | Estudar captura e análise de pacotes | Manual oficial para análise de tráfego | Auxiliou na compreensão da análise de pacotes |

---

## 🧠 Estratégia de Aprendizagem

O NotebookLM foi utilizado como um ambiente de estudo, permitindo:

- sintetizar conteúdos;
- comparar conceitos entre diferentes fontes;
- identificar lacunas de conhecimento;
- construir glossários;
- criar perguntas de revisão;
- validar respostas com base exclusivamente nas fontes carregadas.

O objetivo não foi substituir o estudo tradicional, mas potencializá-lo por meio da Inteligência Artificial.

---

## 🤖 Engenharia de Prompts

Durante o desenvolvimento do projeto foram realizados diversos testes para compreender como pequenas alterações na formulação e na técnica de prompting influenciam a qualidade das respostas.

### Exemplo 1 — Zero-shot → Role Prompting + Estrutura

**Técnica inicial:** Zero-shot (pergunta direta, sem persona nem estrutura).

**Prompt Inicial**
> "Com base exclusivamente nas fontes carregadas, faça um resumo estruturado dos principais fundamentos de cibersegurança necessários para compreender e montar laboratórios práticos."

**Resultado obtido:** Resposta organizada em 5 pilares (Governança/NIST, Exploração de Redes/Nmap, Análise de Tráfego/Wireshark, Segurança de Aplicações/OWASP, Configuração de Laboratório), cobrindo os fundamentos de forma correta, porém genérica.

**Problema encontrado:** Resposta correta, mas rasa — sem comparação entre fontes, sem aprofundamento crítico.

**Técnica refinada:** Role Prompting + Context Engineering (persona de analista + restrição às fontes carregadas + estrutura de resposta definida).

**Prompt Refinado**
> "Atue como um analista especialista em Cibersegurança e pesquisador acadêmico, utilizando exclusivamente as fontes carregadas neste NotebookLM. Sua tarefa é analisar e comparar como diferentes documentos abordam os conceitos fundamentais de segurança da informação: Ameaça, Vulnerabilidade, Risco e Ataque. [...] Organize a resposta em: Introdução, Análise Individual dos Conceitos (definição por fonte, semelhanças, diferenças, exemplos), Comparação Geral em tabela, Relação entre os Conceitos, Exemplos Práticos, Glossário Final e Reflexão Final. Regras: use somente as fontes carregadas, não invente definições, indique a fonte de cada informação, e caso haja divergência entre fontes, apenas explique — não escolha uma como correta."

**Resultado obtido:** Análise comparativa completa cruzando NIST CSF 2.0, OWASP Top 10, WSTG, Nmap e Wireshark para os 4 conceitos, incluindo uma cadeia causal aplicada (Ameaça → Vulnerabilidade → Ataque → Risco) com um cenário real de amplificação DNS, tabela comparativa e glossário derivado das próprias fontes.

**Aprendizado:** Adicionar persona, restringir explicitamente às fontes carregadas e definir a estrutura de saída gera respostas muito mais completas, comparáveis e alinhadas ao material estudado do que um pedido genérico de resumo.

---

### Exemplo 2 — Few-shot Prompting

**Técnica:** Few-shot (fornecer exemplos resolvidos para guiar o padrão de resposta).

**Prompt**
> "Com base nas fontes carregadas, complete o terceiro caso seguindo exatamente o mesmo padrão dos dois exemplos abaixo:
>
> Caso 1 — Ameaça: acesso não autorizado via porta SSH aberta. Vulnerabilidade: serviço SSH desatualizado (Nmap). Ataque: força bruta de credenciais. Risco: comprometimento do host.
>
> Caso 2 — Ameaça: volume anormal de respostas DNS. Vulnerabilidade: servidor DNS mal configurado. Ataque: DDoS por amplificação DNS. Risco: indisponibilidade do serviço.
>
> Caso 3 — [aplicação web com formulário de login] → complete Ameaça, Vulnerabilidade, Ataque e Risco no mesmo padrão, citando a fonte utilizada."

**Resultado obtido:** O NotebookLM completou o Caso 3 citando a OWASP WSTG como base (ameaça de acesso indevido → vulnerabilidade de falta de rate limiting no login → ataque de força bruta/credential stuffing → risco de comprometimento de contas), mantendo o mesmo formato dos exemplos fornecidos.

**Problema encontrado:** Na primeira tentativa, sem indicar "cite a fonte utilizada" no final, o modelo completou o padrão mas sem referência — foi necessário adicionar essa instrução explicitamente.

**Aprendizado:** Fornecer exemplos resolvidos (few-shot) é eficaz para padronizar a estrutura da resposta, mas é preciso reforçar explicitamente regras de atribuição de fonte a cada novo pedido, mesmo que já tenham sido dadas antes na conversa.

---

### Exemplo 3 — Chain of Thought

**Técnica:** Chain of Thought (pedir raciocínio passo a passo antes da resposta final).

**Prompt**
> "Antes de gerar o glossário final, pense passo a passo, nesta ordem: (1) identifique o ativo que está sendo protegido em cada fonte; (2) identifique qual é a exposição ou fraqueza descrita; (3) identifique qual vetor de ataque essa fraqueza permite; (4) só então defina o termo de forma resumida com base nesse raciocínio. Mostre esse raciocínio para os termos Hardening e Superfície de Ataque antes de gerar a definição final de cada um."

**Resultado obtido:** O modelo detalhou o raciocínio intermediário (ex.: para "Superfície de Ataque" — ativo: sistema exposto; exposição: serviços/portas desnecessários ativos identificáveis via Nmap; vetor: qualquer ponto de entrada não removido) antes de consolidar a definição final, o que tornou o glossário mais rastreável às fontes.

**Problema encontrado:** As respostas ficaram mais longas e exigiram divisão em duas rodadas (um termo por vez) para não perder profundidade.

**Aprendizado:** Chain of Thought aumenta a rastreabilidade do raciocínio (útil para justificar decisões, como em um relatório técnico), mas tem custo de verbosidade — vale a pena aplicar em termos-chave, não no glossário inteiro.

---

## ⚠️ Cicatrizes (Troubleshooting)

Durante o desenvolvimento do projeto foram observadas as seguintes dificuldades:

| Situação | Solução |
|---|---|
| Prompts muito genéricos produziram respostas superficiais | Inserção de contexto, persona e objetivo específico |
| Perguntas amplas misturavam conceitos de diferentes documentos | Solicitação explícita para utilizar apenas as fontes carregadas |
| Algumas respostas omitiram detalhes importantes | Divisão da pergunta em partes menores |
| Few-shot sem instrução de atribuição de fonte | Reforço explícito da regra "cite a fonte" em cada novo prompt |
| Chain of Thought gerando respostas longas demais | Divisão em rodadas menores, um termo por vez |

Essas dificuldades demonstraram a importância da engenharia de prompts como parte do processo de aprendizagem — o resultado final depende diretamente de quão bem o problema é formulado.

---

## 📒 Miniguia de Estudos

### Conceitos Fundamentais
- Confidencialidade
- Integridade
- Disponibilidade
- Autenticação
- Autorização
- Não Repúdio

### Principais Ameaças
- Malware
- Phishing
- Engenharia Social
- Ransomware
- Ataques de força bruta

### Ferramentas Estudadas
- Nmap
- Wireshark

### Frameworks
- OWASP Top 10
- OWASP WSTG
- NIST CSF 2.0

---

## 📖 Glossário

| Termo | Definição |
|---|---|
| **CIA Triad** | Modelo composto por Confidencialidade, Integridade e Disponibilidade. |
| **Firewall** | Dispositivo ou software responsável por controlar o tráfego entre redes. |
| **IDS** | Sistema de Detecção de Intrusão. |
| **IPS** | Sistema de Prevenção de Intrusão. |
| **Hardening** | Processo de fortalecimento da segurança de um sistema, reduzindo pontos de exposição. |
| **Superfície de Ataque** | Conjunto de pontos que podem ser explorados por um atacante. |
| **CVE** | Identificador público de vulnerabilidades conhecidas. |
| **CVSS** | Sistema utilizado para classificar a gravidade de vulnerabilidades. |

---

## 💬 Prompts Reutilizáveis

- "Explique este conceito utilizando apenas as fontes carregadas."
- "Compare os conceitos apresentados por diferentes documentos."
- "Quais informações aparecem em todas as fontes?"
- "Quais divergências existem entre os documentos?"
- "Crie dez perguntas de revisão baseadas exclusivamente nas fontes."
- "Monte um mapa mental sobre este assunto."
- "Gere um glossário contendo os principais termos técnicos."
- "Quais conhecimentos prévios são necessários para compreender este tema?"
- "Complete o próximo caso seguindo exatamente o mesmo padrão dos exemplos anteriores, citando a fonte utilizada." *(few-shot)*
- "Antes de responder, pense passo a passo: identifique o ativo, a exposição, o vetor de ataque e só então gere a definição final." *(chain of thought)*

---

## 💡 Lições Aprendidas

Ao longo deste projeto foi possível perceber que a qualidade das respostas geradas pela IA depende diretamente da qualidade das perguntas realizadas.

Também ficou evidente que:

- boas fontes produzem melhores respostas;
- prompts específicos, com persona e estrutura definida, geram respostas mais úteis do que pedidos genéricos;
- técnicas como few-shot e chain of thought têm aplicações e custos diferentes (few-shot exige atenção à atribuição de fonte; CoT exige controle de verbosidade);
- documentar erros faz parte do processo de aprendizagem;
- o NotebookLM funciona melhor quando utilizado como ferramenta de apoio ao estudo, e não como substituto do raciocínio crítico.

---

## 🚀 Conclusão

O desenvolvimento deste projeto demonstrou que a Inteligência Artificial pode atuar como uma importante ferramenta de aprendizagem ativa quando utilizada de forma consciente e estruturada.

A combinação entre curadoria de fontes confiáveis, engenharia de prompts e documentação do processo permitiu construir um material reutilizável para estudos futuros e reforçou a importância da validação crítica das respostas geradas pela IA.

---

## 🚀 Próximos Passos

- Expandir o caderno com novos frameworks de segurança.
- Adicionar estudos sobre SIEM e SOC.
- Comparar respostas do NotebookLM com outros modelos de IA.
- Atualizar o conteúdo conforme novas versões das fontes oficiais.

---

## 👨‍💻 Autor

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/edudsprado" title="Perfil Eduardo">
        <img src="https://avatars.githubusercontent.com/u/203672299?v=4" width="200px;" alt="Eduardo Prado"/><br>
        <sub>
          <b>Eduardo Prado</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

Projeto desenvolvido para o desafio da **Digital Innovation One (DIO)** com foco na utilização do NotebookLM como ferramenta de aprendizagem ativa em Cibersegurança.
