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

- Sobre o Projeto
- Objetivos
- Curadoria das Fontes
- Estratégia de Aprendizagem
- Engenharia de Prompts
- Cicatrizes (Troubleshooting)
- Miniguia de Estudos
- Glossário
- Prompts Reutilizáveis
- Lições Aprendidas
- Considerações Finais
- Autor

# 🎯 Objetivos

## Objetivo Geral

Construir um caderno temático utilizando o NotebookLM para organizar, compreender e revisar conceitos fundamentais de cibersegurança aplicados à criação de laboratórios práticos.

## Objetivos Específicos

- compreender os princípios fundamentais da segurança da informação;
- identificar ameaças, vulnerabilidades e mecanismos de proteção;
- aprender a utilizar fontes técnicas oficiais como base de estudo;
- experimentar diferentes estratégias de prompts no NotebookLM;
- documentar os resultados obtidos durante o processo de aprendizagem;
- produzir um miniguia reutilizável para estudos futuros.

---

# 📚 Curadoria das Fontes

Foram selecionadas cinco fontes oficiais e amplamente reconhecidas na área de Segurança da Informação.

| Fonte | Objetivo | Justificativa | Contribuição para NotebookLM |
|--------|----------|---------------|------------------------------|
| OWASP Top 10 | Estudar as principais vulnerabilidades em aplicações web | Principal referência mundial sobre riscos de segurança em aplicações | Permitiu comparar riscos comuns em aplicações web. |
| OWASP Web Security Testing Guide (WSTG) | Compreender metodologias de testes de segurança | Complementa o Top 10 com procedimentos práticos | Forneceu metodologia prática para validação de segurança. |
| NIST Cybersecurity Framework (CSF 2.0) | Estudar boas práticas e governança em segurança | Framework utilizado internacionalmente | Relacionou conceitos técnicos com gestão de segurança. |
| Documentação Oficial do Nmap | Aprender reconhecimento de redes | Referência oficial da ferramenta | Serviu de base para estudos sobre mapeamento de redes. |
| Wireshark User's Guide | Estudar captura e análise de pacotes | Manual oficial para análise de tráfego | Auxiliou na compreensão da análise de pacotes. |
---

# 🧠 Estratégia de Aprendizagem

O NotebookLM foi utilizado como um ambiente de estudo, permitindo:

- sintetizar conteúdos;
- comparar conceitos entre diferentes fontes;
- identificar lacunas de conhecimento;
- construir glossários;
- criar perguntas de revisão;
- validar respostas com base exclusivamente nas fontes carregadas.

O objetivo não foi substituir o estudo tradicional, mas potencializá-lo por meio da Inteligência Artificial.

---

# 🤖 Engenharia de Prompts

Durante o desenvolvimento do projeto foram realizados diversos testes para compreender como pequenas alterações na formulação dos prompts influenciam a qualidade das respostas.

## Exemplo 1

### Prompt Inicial

> Com base exclusivamente nas fontes carregadas, faça um resumo estruturado dos principais fundamentos de cibersegurança necessários para compreender e montar laboratórios práticos..

### Resultado

Para compreender e montar laboratórios práticos de cibersegurança eficazes, é essencial dominar os fundamentos que abrangem desde a governança estratégica até a análise técnica profunda de redes e aplicações. Com base nas fontes fornecidas, os principais pilares são:
1. Governança e Gestão de Riscos (NIST CSF 2.0)
O ponto de partida para qualquer ambiente de segurança é o entendimento e a melhoria da gestão de riscos
.
Ações Práticas: O framework traduz objetivos de alto nível em ações para mitigar riscos, como eventos de ransomware
.
Conformidade e Automação: É necessário alinhar configurações de produtos de TI com resultados do framework para permitir relatórios e automação baseados em evidências
.
2. Exploração de Redes e Inventário (Nmap)
Antes de proteger ou testar um ambiente, deve-se realizar a exploração de rede e auditoria de segurança
.
Descoberta de Hosts e Serviços: Identificar quais hosts estão ativos, quais serviços (aplicação e versão) eles oferecem e quais sistemas operacionais estão executando
.
Estados de Porta: Compreender a "tabela de portas interessantes" e seus estados: open (aplicação escutando), closed (sem aplicação), filtered (bloqueada por firewall/filtro) ou unfiltered (o Nmap não consegue determinar o estado)
.
Auditoria: Utilizar pacotes IP em estado bruto para determinar o inventário de rede e a disponibilidade do serviço
.
3. Análise de Tráfego e Protocolos (Wireshark)
A análise detalhada do tráfego permite "medir" o que acontece dentro dos cabos de rede
.
Captura e Inspeção: Realizar capturas ao vivo em diversos meios (Ethernet, Wi-Fi, Bluetooth) e inspecionar o conteúdo dos pacotes com dissecação profunda de protocolos
.
Diagnóstico de Anomalias: Utilizar o Expert Info para identificar automaticamente comportamentos incomuns ou problemas de rede, classificados por severidade (Chat, Note, Warn, Error)
.
Análise de Fluxo (TCP): Rastrear o estado de sessões TCP para detectar problemas como retransmissões, perdas de pacotes ou janelas cheias (ZeroWindow)
.
Remontagem de Dados: Compreender como protocolos de nível superior (como HTTP) dividem dados em múltiplos pacotes e como o Wireshark os remonta para análise do conteúdo original
.
4. Segurança de Aplicações Web (OWASP)
O foco na camada de aplicação é vital, dado que as vulnerabilidades web são vetores críticos.
Riscos Críticos: O padrão de referência é o OWASP Top 10, que lista os riscos de segurança mais críticos para aplicações web e serve como guia para o desenvolvimento de código seguro
.
Metodologia de Teste: O Web Security Testing Guide (WSTG) fornece uma estrutura abrangente de melhores práticas utilizadas por testadores de invasão e organizações em todo o mundo para validar a segurança de serviços web
.
5. Configuração e Ferramental de Laboratório
Para a montagem prática, as fontes destacam requisitos técnicos:
Privilégios: O acesso root ou administrador é frequentemente necessário para capturas de pacotes e varreduras brutas
.
Ambiente de Captura: Escolher a interface correta e estar no "lugar certo" da rede para visualizar o tráfego desejado
.
Tratamento de Dados: Em laboratórios colaborativos, é importante sanitizar capturas (ex: com TraceWrangler) para não expor informações sensíveis ou PII (Informações de Identificação Pessoal).

### Problema

Nenhum aparente, além de um resposta genérica e rápida.

### Prompt Refinado

> Atue como um analista especialista em Cibersegurança e pesquisador acadêmico, utilizando exclusivamente as fontes carregadas neste NotebookLM.

Sua tarefa é analisar e comparar como diferentes documentos abordam os conceitos fundamentais de segurança da informação:

Ameaça (Threat)
Vulnerabilidade (Vulnerability)
Risco (Risk)
Ataque (Attack)

O objetivo é criar um material de estudo estruturado para um Caderno Temático de Cibersegurança, destacando diferenças de interpretação, pontos em comum e aplicações práticas.

Instruções de Análise

Para cada conceito, identifique nas fontes:

A definição apresentada.
Como o conceito é explicado.
Quais características principais são destacadas.
Quais exemplos práticos aparecem.
Como o conceito se relaciona com os demais elementos da segurança da informação.
Comparação Entre as Fontes

Crie uma análise comparativa mostrando:

Semelhanças

Identifique:

definições semelhantes;
ideias compartilhadas;
conceitos que aparecem em diferentes documentos;
princípios comuns entre os autores.
Diferenças

Destaque:

mudanças na forma de explicar o conceito;
diferentes níveis de profundidade;
abordagens técnicas ou gerenciais;
diferenças de terminologia.

Explique por que essas diferenças podem existir quando houver evidências nas fontes.

Estrutura da Resposta

Organize a resposta no seguinte formato:

1. Introdução

Explique a importância desses conceitos dentro da cibersegurança.

2. Análise Individual dos Conceitos

Para cada conceito:

Ameaça
Definições encontradas nas fontes:
Fonte 1:
Fonte 2:
Fonte 3:
Pontos em comum:
Diferenças:
Exemplos práticos encontrados:

Repita a mesma estrutura para:

Vulnerabilidade
Risco
Ataque
3. Comparação Geral

Crie uma tabela:

Conceito	Como as fontes definem	Principais semelhanças	Principais diferenças
Ameaça			
Vulnerabilidade			
Risco			
Ataque			
4. Relação Entre os Conceitos

Explique como os conceitos se conectam em um cenário real de segurança:

Exemplo de estrutura:

Ameaça → Explora → Vulnerabilidade → Realiza um Ataque → Gera Impacto → Representa um Risco

Explique essa relação utilizando exemplos citados nas fontes.

5. Exemplos Práticos

Liste exemplos encontrados nos documentos:

Cenário:

Explique:

Qual é a ameaça?
Qual vulnerabilidade foi explorada?
Qual ataque ocorreu?
Qual risco foi gerado?
6. Glossário Final

Crie um glossário contendo:

Termo	Definição resumida	Exemplo
Ameaça		
Vulnerabilidade		
Risco		
Ataque		
7. Reflexão Final

Finalize respondendo:

Qual conceito aparece com maior destaque nas fontes?
Qual conceito possui maior diferença de interpretação?
Por que compreender esses conceitos é importante para profissionais de cibersegurança?
Como esse conhecimento pode ser aplicado na criação de laboratórios práticos?
Regras Importantes
Utilize somente informações presentes nas fontes carregadas.
Não invente definições que não aparecem nos documentos.
Sempre indique de qual fonte a informação foi retirada.
Caso as fontes apresentem divergências, não escolha uma como correta; apenas explique as diferenças.
Priorize uma explicação clara para estudantes iniciantes em cibersegurança.

### Aprendizado

Adicionar contexto e restringir as fontes gera respostas mais completas e alinhadas ao material estudado.

### Resultado

Este Caderno Temático de Cibersegurança foi estruturado para fornecer uma base sólida a estudantes iniciantes, comparando visões que vão da gestão estratégica de riscos à análise técnica de pacotes.
1. Introdução
A compreensão dos conceitos fundamentais de ameaça, vulnerabilidade, risco e ataque é o alicerce da cibersegurança. Sem uma definição clara desses termos, as organizações falham em priorizar defesas e os profissionais técnicos perdem a capacidade de diagnosticar problemas com precisão. Enquanto frameworks de governança utilizam esses conceitos para gerir o impacto no negócio
, ferramentas de análise os aplicam para identificar falhas técnicas e comportamentos anômalos no tráfego de rede
.
2. Análise Individual dos CONCEITOS
Ameaça (Threat)
Definições encontradas nas fontes:
Fonte 1 (NIST): Enfocada na gestão estratégica, cita especificamente eventos de ransomware como ameaças que devem ser geridas e mitigadas de forma proativa
.
Fonte 2 (Wireshark): Aborda ameaças como comportamentos "estranhos" ou anomalias de segurança na rede que o analista deve investigar para entender o que realmente está acontecendo
.
Fonte 3 (OWASP): Foca em ameaças direcionadas à camada de aplicação web que buscam explorar riscos críticos de segurança
.
Pontos em comum: Todas as fontes tratam a ameaça como um agente ou evento externo/interno com potencial para causar danos ou instabilidade ao ambiente
.
Diferenças: O NIST aborda a ameaça sob a ótica de gestão e governança
, enquanto o Wireshark a visualiza como uma métrica técnica de tráfego (ex: pacotes malformados)
.
Exemplos práticos encontrados: Eventos de ransomware
, tráfego de negação de serviço (DDoS) baseado em DNS
 e comandos de controle ou tunelamento
.
Vulnerabilidade (Vulnerability)
Definições encontradas nas fontes:
Fonte 1 (Nmap): Identifica vulnerabilidades técnicas através da exposição de portas abertas, serviços desatualizados e versões de sistemas operacionais vulneráveis
.
Fonte 2 (OWASP WSTG): Define vulnerabilidades como "fraquezas" específicas no código ou na configuração de aplicações web, categorizando-as em cenários de teste
.
Fonte 3 (Wireshark): Visualiza vulnerabilidades como violações de especificações de protocolo ou erros de implementação que causam pacotes malformados
.
Pontos em comum: A vulnerabilidade é invariavelmente vista como uma fraqueza interna ou falha de configuração que pode ser explorada
.
Diferenças: O Nmap foca na vulnerabilidade da infraestrutura de rede (portas/serviços)
, enquanto a OWASP foca na lógica de aplicação e código-fonte
.
Exemplos práticos encontrados: Porta 22/tcp aberta com software desatualizado
, falhas de injeção em sites web
 e erros de soma de verificação (checksum) inválidos
.
Risco (Risk)
Definições encontradas nas fontes:
Fonte 1 (NIST): O framework é desenhado para "entender e melhorar a gestão de risco de cibersegurança", traduzindo objetivos estratégicos em ações práticas de mitigação
.
Fonte 2 (OWASP Top 10): Define risco pela criticidade do impacto negativo que uma vulnerabilidade web pode causar na cultura de desenvolvimento e no software
.
Fonte 3 (Wireshark): O risco técnico é medido pela severidade das anomalias encontradas no tráfego através do recurso Expert Info (severidades: Chat, Note, Warn, Error)
.
Pontos em comum: O risco é tratado como a medida de probabilidade e impacto de um evento negativo
.
Diferenças: O NIST adota uma abordagem de risco organizacional
, enquanto o Wireshark adota uma abordagem de risco operacional/técnico imediato
.
Exemplos práticos encontrados: Adoção do OWASP Top 10 como primeiro passo para mitigar riscos
 e identificação de erros sérios de protocolo (nível Error)
.
Ataque (Attack)
Definições encontradas nas fontes:
Fonte 1 (OWASP WSTG): Fornece uma estrutura de "melhores práticas" para que testadores de invasão (penetration testers) realizem ataques controlados para validar a segurança
.
Fonte 2 (Nmap): Frequentemente utilizado na fase de reconhecimento de um ataque para auditar firewalls e filtros de pacotes
.
Fonte 3 (Wireshark): Não detecta o ataque ativamente (não é um IDS), mas permite medir e analisar os efeitos do ataque "no cabo"
.
Pontos em comum: O ataque é a execução da exploração contra um alvo
.
Diferenças: O WSTG foca na metodologia do ataque para testes
, enquanto o Wireshark foca na medição do impacto e análise forense pós-evento
.
Exemplos práticos encontrados: Auditoria de segurança contra hosts individuais
, testes de coleta de informações (WSTG-INFO-02)
 e análise de fluxos TCP suspeitos
.
3. Comparação Geral
Conceito
Como as fontes definem
Principais semelhanças
Principais diferenças
Ameaça
Agente externo ou evento (ex: Ransomware)
.
Potencial de dano.
NIST (Gestão) vs. Wireshark (Tráfego técnico)
.
Vulnerabilidade
Fraquezas técnicas (portas)
 ou lógicas (web)
.
É uma falha interna.
Nmap (Rede/OS)
 vs. OWASP (Aplicação)
.
Risco
Gestão organizacional
 ou criticidade de falhas
.
Foco no impacto e perda.
NIST (Negócio) vs. Wireshark (Severidade técnica)
.
Ataque
Execução de exploração/testes
 ou reconhecimento
.
Exploração ativa da falha.
WSTG (Metodologia)
 vs. Wireshark (Medição passiva)
.
4. Relação Entre os Conceitos
Em um cenário real, os conceitos se conectam de forma cíclica: Ameaça (ex: Atacante externo) → Explora → Vulnerabilidade (ex: Porta SSH aberta identificada pelo Nmap
) → Realiza um Ataque (ex: Brute force simulado via guia WSTG
) → Gera Impacto (ex: Retransmissões e anomalias capturadas pelo Wireshark
) → Representa um Risco (ex: Comprometimento de dados gerido pelo framework NIST
).
5. Exemplos Práticos
Cenário: Investigação de Saúde de Serviço DNS
Ameaça: Volume anormal de respostas DNS significativamente maiores que as requisições
.
Vulnerabilidade: Configuração inadequada do servidor DNS que permite amplificação ou não valida consultas
.
Ataque: Ataque de Negação de Serviço Distribuída (DDoS) baseado em DNS ou Tunelamento DNS para Comando e Controle
.
Risco: Indisponibilidade do serviço ou exfiltração de dados (PII), gerando alto nível de severidade no Expert Info do Wireshark
.
6. Glossário Final
Termo
Definição resumida
Exemplo
Ameaça
Agente ou evento com potencial de causar dano
.
Ransomware
.
Vulnerabilidade
Fraqueza interna técnica ou lógica no sistema
.
Porta aberta ou software obsoleto
.
Risco
Probabilidade de perda ou impacto negativo gerido pela organização
.
Criticidade nível "Error" em protocolos
.
Ataque
Ação de explorar vulnerabilidades para atingir um objetivo
.
Teste de Invasão (Pentest)
.
7. Reflexão Final
Conceito com maior destaque: O Risco aparece com maior ênfase, pois tanto o NIST CSF 2.0 quanto o OWASP Top 10 são estruturados inteiramente em torno da melhoria da gestão e priorização de riscos
.
Maior diferença de interpretação: A Vulnerabilidade. Para o Nmap, ela é uma porta aberta ou um serviço visível
; para a OWASP, é uma falha na lógica do código web
; para o Wireshark, é um erro de conformidade de protocolo (pacote malformado)
.
Importância para profissionais: Compreender esses conceitos permite que o analista fale a linguagem da gestão (NIST) enquanto executa a validação técnica (WSTG/Nmap) e diagnósticos precisos (Wireshark)
.
Aplicação em laboratórios: Esse conhecimento permite montar laboratórios que não apenas "rodam ferramentas", mas que simulam o ciclo completo: configurar uma vulnerabilidade (OWASP), descobrir o alvo (Nmap), realizar o ataque (WSTG) e medir o resultado (Wireshark) sob uma governança de riscos (NIST)

---

# ⚠️ Cicatrizes (Troubleshooting)

Durante o desenvolvimento do projeto foram observadas algumas dificuldades.

| Situação | Solução |
|----------|----------|
| Prompts muito genéricos produziram respostas superficiais | Inserção de contexto e objetivo específico |
| Perguntas amplas misturavam conceitos de diferentes documentos | Solicitação para utilizar apenas as fontes carregadas |
| Algumas respostas omitiram detalhes importantes | Divisão da pergunta em partes menores |

Essas dificuldades demonstraram a importância da engenharia de prompts como parte do processo de aprendizagem.

---

# 📒 Miniguia de Estudos

## Conceitos Fundamentais

- Confidencialidade
- Integridade
- Disponibilidade
- Autenticação
- Autorização
- Não Repúdio

## Principais Ameaças

- Malware
- Phishing
- Engenharia Social
- Ransomware
- Ataques de força bruta

## Ferramentas Estudadas

- Nmap
- Wireshark

## Frameworks

- OWASP Top 10
- OWASP WSTG
- NIST CSF 2.0

---

# 📖 Glossário

**CIA Triad** — Modelo composto por Confidencialidade, Integridade e Disponibilidade.

**Firewall** — Dispositivo ou software responsável por controlar o tráfego entre redes.

**IDS** — Sistema de Detecção de Intrusão.

**IPS** — Sistema de Prevenção de Intrusão.

**Hardening** — Processo de fortalecimento da segurança de um sistema.

**Superfície de Ataque** — Conjunto de pontos que podem ser explorados por um atacante.

**CVE** — Identificador público de vulnerabilidades conhecidas.

**CVSS** — Sistema utilizado para classificar a gravidade de vulnerabilidades.

---

# 💬 Prompts Reutilizáveis

- Explique este conceito utilizando apenas as fontes carregadas.
- Compare os conceitos apresentados por diferentes documentos.
- Quais informações aparecem em todas as fontes?
- Quais divergências existem entre os documentos?
- Crie dez perguntas de revisão baseadas exclusivamente nas fontes.
- Monte um mapa mental sobre este assunto.
- Gere um glossário contendo os principais termos técnicos.
- Quais conhecimentos prévios são necessários para compreender este tema?

---

# 💡 Lições Aprendidas

Ao longo deste projeto foi possível perceber que a qualidade das respostas geradas pela IA depende diretamente da qualidade das perguntas realizadas.

Também ficou evidente que:

- boas fontes produzem melhores respostas;
- prompts específicos geram respostas mais úteis;
- documentar erros faz parte do processo de aprendizagem;
- o NotebookLM funciona melhor quando utilizado como ferramenta de apoio ao estudo, e não como substituto do raciocínio crítico.

---

# 🚀 Conclusão

O desenvolvimento deste projeto demonstrou que a Inteligência Artificial pode atuar como uma importante ferramenta de aprendizagem ativa quando utilizada de forma consciente e estruturada.

A combinação entre curadoria de fontes confiáveis, engenharia de prompts e documentação do processo permitiu construir um material reutilizável para estudos futuros e reforçou a importância da validação crítica das respostas geradas pela IA.

---

# 🚀 Próximos Passos

- Expandir o caderno com novos frameworks de segurança.
- Adicionar estudos sobre SIEM e SOC.
- Comparar respostas do NotebookLM com outros modelos de IA.
- Atualizar o conteúdo conforme novas versões das fontes oficiais.

# 👨‍💻 Autor


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
