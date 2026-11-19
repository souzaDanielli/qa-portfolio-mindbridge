# Portfólio de Testes: MindBridge

Documentos de teste de software que elaborei como prática do curso **Junior QA / Software Tester (Microsoft)**, aplicados à aplicação de treinamento **MindBridge** (plataforma de matrícula em cursos e tutoria).

> MindBridge é uma aplicação educacional usada nos laboratórios do curso. Este repositório contém apenas os documentos de teste que eu produzi. Os documentos estão em português.

## Conteúdo

| Pasta | Documento | O que demonstra |
|---|---|---|
| [`01-cobertura-de-testes`](01-cobertura-de-testes/) | Documento de Cobertura de Testes | Planejamento: tipos de teste, ambientes e critérios de aprovação/reprovação |
| [`02-estrategia-qa-e-bdd`](02-estrategia-qa-e-bdd/) | Estratégia QA e BDD | Estratégia STLC, critérios de aceitação em BDD e registro de defeitos com evidências |
| [`03-testes-exploratorios-e-relatorio-de-bug`](03-testes-exploratorios-e-relatorio-de-bug/) | Testes Exploratórios e Relatório de Bug | Sessão exploratória, relatório de bug no Jira e recuperação de ticket rejeitado |

## Resumo por documento

### 01. Documento de Cobertura de Testes
- **Escopo:** fluxo de inscrição em cursos e tutores (catálogo, carrinho e simulação de checkout).
- **Tipos de teste:** funcionais, tratamento de erros/negativos, regressão, usabilidade e design responsivo.
- **Para cada tipo:** descrição, ambiente (QA em `localhost:8081` ou STAGING em `localhost:8082`), justificativa do ambiente e critérios de aprovação/reprovação.
- **Defeitos conhecidos documentados:** DEF-001 e DEF-002 (veja a tabela abaixo).

### 02. Estratégia QA e BDD
- Técnicas estáticas (revisão de requisitos e dos critérios de aceitação) e dinâmicas (testes funcionais e negativos, UI responsiva e API com DevTools).
- Ambiente de homologação (Staging em `localhost:3000`).
- Critérios de aceitação em **BDD (Given-When-Then)** para a história de usuário de compartilhamento do painel, com três cenários: caminho feliz, caso de borda (mobile) e condição de erro (nota vazia).
- Log de defeitos com passos para reproduzir, resultado esperado, resultado obtido, severidade e evidências.

### 03. Testes Exploratórios e Relatório de Bug
- Sessão de testes exploratórios de cerca de 15 minutos no fluxo de checkout, com as heurísticas *Rapid Input*, *Unexpected Characters*, *Boundary / Goldilocks* e *Interruption*.
- Relatório de bug no Jira: checkout aceita data de validade inválida.
- Recuperação de um ticket rejeitado como *Cannot Reproduce*, com as mudanças feitas e o motivo de cada uma.

## Defeitos registrados

| Documento | Defeito | Severidade registrada |
|---|---|---|
| 01 | **DEF-001:** erro HTTP 500 ao inserir caractere especial (ex.: `@`) no campo de pagamento | Não informada (defeito conhecido) |
| 01 | **DEF-002:** menu de navegação sobreposto ao conteúdo em telas abaixo de 400 px | Não informada (defeito conhecido) |
| 02 | API retorna HTTP 500 quando a nota de compartilhamento está vazia | Medium |
| 02 | Banner de confirmação sobrepõe o cabeçalho em viewport mobile | Medium |
| 03 | Checkout aceita data de validade inválida (`32/12`) | Major |
| 03 | Dados do formulário não são mantidos ao voltar/avançar no navegador, e a barra de navegação fica inutilizável em viewport reduzida | Descritos na sessão exploratória |

## Ferramentas e técnicas
Jira, Chrome DevTools (Network), BDD (Given-When-Then), STLC, testes funcionais, negativos e exploratórios.

## Complemento: testes automatizados
Para um exemplo de automação, veja os testes de API com pytest e TestClient do projeto [ASAC](https://github.com/souzaDanielli/ASAC).

## Autora
Danielli Souza Silva · [LinkedIn](https://www.linkedin.com/in/daniellisilvadev/) · [GitHub](https://github.com/souzaDanielli)