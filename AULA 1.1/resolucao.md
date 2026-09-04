# Atividades — Aula 1.1: Introdução à Modelagem de Domínio

**Disciplina:** Modelagem de Domínio
**Professor:** Victor Sobreira
**Aluna:** Geovanna de Oliveira Xavier — 32421BSI006
**Curso:** Bacharelado em Sistemas de Informação (BSI) — UFU

---

## Atividade 1 — Conceito de Modelos

> Tente lembrar de modelos que você já tenha visto, usado ou experimentado. Indique ao menos três mais relevantes, comente brevemente seu propósito/utilidade e descreva suas características específicas e comuns com os demais.

### Modelo 1: _[Diagrama de Entidade-Relacionamento]_

- **Propósito/utilidade:**Foi utilizado na disciplina de Bando de Dados.O proposito é planejar a estrutura antes de criar o código SQL.Utilizado para representar entidades,atributos e com se relacionam enter si.
- **Características (simplicidade, abstração, analogia, formalidade):**Ignora regras de código, mostra só a estrutura de dados , Foca nas entidades e relacionamentos essenciais do sistema, Segue notação formal (Entidade-Relacionamento, cardinalidades).

### Modelo 2: _[Google Maps]_

- **Propósito/utilidade:**Uso esse modelo praticamente todo dia pra me localizar. O propósito é representar ruas, distâncias e trajetos possíveis entre dois pontos, permitindo escolher o caminho mais rápido.
- **Características:**Foca só em ruas, distâncias e sentido do trânsito. Usa linhas coloridas pra representar ruas reais. Usa uma simbologia própria e padronizada (setas, ícones).


---

## Atividade 2 — Exemplos de Modelos Gerais

> Com base nos exemplos vistos em aula, lembre de outros modelos semelhantes que te marcaram (três exemplos). Comente brevemente propósito/utilidade e indique como ajudaram a compreender com maior clareza os sistemas, processos ou conceitos envolvidos, destacando vantagens e desvantagens.

### Modelo 1: _[Mapa de uma cidade]_

- **Propósito/utilidade:**Facilitar a localização de lugares e o planejamento de trajetos.
- **Como ajudou a compreender:**Permitiu visualizar ruas, bairros e locais sem precisar conhecer a cidade pessoalmente.
- **Vantagens:**É simples, visual e facilita a orientação
- **Desvantagens:**Não representa todos os detalhes da cidade.

### Modelo 2: _[Mapa de rotas de aviões]_

- **Propósito/utilidade:**Mostrar as rotas e conexões entre diferentes aeroportos e cidades.
- **Como ajudou a compreender:**Facilitou a visualização dos caminhos percorridos pelos aviões.
- **Vantagens:**Permite visualizar várias rotas de forma rápida e organizada.
- **Desvantagens:**Pode não aparecer alguns aviões particulares.

### Modelo 3: _[Fluxograma ]_

- **Propósito/utilidade:**Representar as etapas e decisões de um processo.
- **Como ajudou a compreender:**Mostrou de forma visual a sequência em que as atividades acontecem.
- **Vantagens:**Facilita a compreensão e identificação das etapas.
- **Desvantagens:**Pode ficar complexo quando o processo possui muitas etapas e decisões.

---

## Atividade 3 — Representando Modelos Computacionais

> Considerando um segundo algoritmo de ordenação (ex. Quick Sort), revise o algoritmo e explique-o usando diferentes perspectivas: (1) linguagem natural, (2) diagramas livres, (3) pseudo-código ou código, (4) diagrama formal (UML, DFD, ...). Compare as explicações quanto a clareza, público-alvo, curva de aprendizado, recursos disponíveis e contexto de aplicação.

### 1. Linguagem natural

_[O Quick Sort também segue a lógica de "Dividir para Conquistar", só que de um jeito diferente do Merge Sort. Primeiro, ele escolhe um elemento do vetor como "pivô" (por exemplo, o último elemento). Depois, ele reorganiza o vetor de forma que todos os elementos menores que o pivô fiquem à esquerda dele, e todos os maiores fiquem à direita , esse processo é chamado de "particionamento". Depois disso, o pivô já está na posição final correta. Em seguida, o algoritmo repete esse mesmo processo recursivamente para a parte da esquerda e para a parte da direita, até que cada pedacinho do vetor tenha só um elemento (que já está automaticamente ordenado). No final, juntando tudo, o vetor inteiro fica ordenado.]_

### 2. Diagramas livres

_[`./diagrama-livre.png` ]_

### 3. Pseudocódigo ou código

```
[01. quicksort(A[0...n-1], inicio, fim)
02.    se (inicio < fim)
03.       posPivo ← particionar(A, inicio, fim)   // particiona e retorna a posição final do pivô
04.       quicksort(A, inicio, posPivo - 1)         // ordena a parte esquerda
05.       quicksort(A, posPivo + 1, fim)            // ordena a parte direita

06. particionar(A[0...n-1], inicio, fim)
07.    pivo ← A[fim]        // escolhe o último elemento como pivô
08.    i ← inicio - 1        // índice do último elemento menor que o pivô
09.    para j ← inicio até fim - 1
10.       se (A[j] < pivo)
11.          i ← i + 1
12.          trocar A[i] com A[j]
13.    trocar A[i + 1] com A[fim]   // coloca o pivô na posição correta
14.    retornar i + 1 ]
```

### 4. Diagrama formal (UML, DFD, ...)

_[`./diagrama-formal.png `]_

### Comparação entre as perspectivas

| Perspectiva | Clareza | Público-alvo | Curva de aprendizado | Recursos necessários | Contexto de aplicação |
|---|---|---|---|---|---|
| Linguagem natural |Alta para leigos, mas pode ficar ambígua em detalhes técnicos | Qualquer pessoa, inclusive sem conhecimento técnico|Baixa | Nenhum, só texto |Explicar a ideia geral para stakeholders ou em aula introdutória |
| Diagramas livres | 	Boa para entender a intuição visualmente, mas pouco precisa |Alunos iniciantes, times em brainstorming | Baixa | Papel/quadro, sem ferramenta específica | Fase de rascunho, discussão inicial em equipe |
| Pseudocódigo/código | Alta precisão técnica, mas exige saber ler lógica de programação | Programadores e estudantes de computação| Média/alta | Conhecimento de lógica de programação | Implementação real do algoritmo |
| Diagrama formal |	Alta clareza estrutural, com notação padronizada |Analistas, times técnicos que precisam de documentação | Média | Ferramenta de diagramação e conhecimento da notação | Documentação técnica formal do sistema |

---

## Atividade 4 — Por que Modelar?

> Selecione ao menos três modelos entre os exemplos vistos anteriormente e comente sobre como se adequam aos propósitos da modelagem (Entendimento, Comunicação, Análise, Projeto e Documentação). Sugira representações alternativas que poderiam melhorar ou complementar alguma falha ou fraqueza dessas representações.

### Modelo 1: _[Merge Sort]_

- **Propósitos atendidos:** Entendimento, Comunicação, Análise, Projeto e Documentação. Ajuda a entender as etapas do algoritmo e pode servir como referência para sua implementação.
- **Representação alternativa sugerida:**Um fluxograma, para deixar as etapas do algoritmo mais visuais.

### Modelo 2: _[Diagrama de Classes UML]_

- **Propósitos atendidos:**Entendimento, Comunicação, Análise, Projeto e Documentação. Facilita a visualização das classes, atributos e relacionamentos do sistema.
- **Representação alternativa sugerida:**Um diagrama de sequência, para mostrar melhor a interação entre os elementos.

### Modelo 3: _[Diagrama Entidade-Relacionamento (DER)]_

- **Propósitos atendidos:**Entendimento, Comunicação, Análise, Projeto e Documentação. Ajuda a visualizar as entidades, seus atributos e os relacionamentos entre os dados.
- **Representação alternativa sugerida:**Um modelo lógico do banco de dados, para detalhar a organização dos dados.

---

## Atividade 5 — Conceitos Básicos (App de Entrega de Comida)

> Considere uma aplicação de entrega de comidas. Reflita sobre o seu próprio modelo mental em relação ao funcionamento deste tipo de aplicação.

### 1. Cenário de uso

> Considere um cenário de uso, desde o pedido até a efetivação da entrega. Descreva brevemente seu entendimento.

_[O cliente realiza um pedido pelo aplicativo, escolhe os produtos e efetua o pagamento. O restaurante recebe e prepara o pedido, que depois é encaminhado ao entregador. O entregador realiza a entrega ao cliente, finalizando o pedido.]_

### 2. Elementos do domínio

- **Atores envolvidos:**Cliente, restaurante e entregador.
- **Produtos e artefatos produzidos/manipulados:**Produtos do restaurante, pedido, comprovante de pagamento e entrega.
- **Ações e operações permitidas:**Fazer pedido, escolher produtos, realizar pagamento, aceitar e preparar pedido, retirar e entregar pedido.
- **Relacionamentos entre os elementos:**O cliente realiza um pedido com produtos do restaurante, o restaurante prepara o pedido e o entrega ao entregador, que leva o pedido até o cliente.

### 3. Diagrama ilustrativo

> Crie um diagrama que represente esse modelo mental (pode ser descrito em texto, ou anexado como imagem no repositório).

_[` ./diagrama-delivery.png`]_


---

## Referências

- Slides da Aula 1.1 — prof. Victor Sobreira