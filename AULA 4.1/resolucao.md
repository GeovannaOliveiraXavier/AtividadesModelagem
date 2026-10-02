# Modelagem — Resolução da Atividade Aula 4.1

**Aluno(a):** Geovanna
**Matrícula:** 32421BSI006
**Curso:** Bacharelado em Sistemas de Informação (BSI) — UFU
**Data de entrega:** [02/10/2026]
**Professor(a):** Victor Sobreira

---

## Sumário

- [Atividade:: Diferencial Competitivo](#questão-1---atividade-diferencial-competitivo)
- [Atividade:: Identificar e Classificar Subdomínios (1)](#questão-2---atividade-identificar-e-classificar-subdomínios)
- [Atividade:: Identificar e Classificar Subdomínios (2)](#questão-3---atividade-identificar-e-classificar-subdomínios-2)

---

## Questão 1 - Atividade:: Diferencial Competitivo

**Enunciado:**
> 1. Identifique quais seriam os diferenciais competitivos e subdomínios principais para os seguintes domínios de negócio/empresas:
• Petrobrás
• Nubank
• Tesla
• Netflix

**Resolução:**

**Petrobras**
Diferencial Competitivo: Tecnologia avançada de exploração e produção de petróleo em águas ultraprofundas (camada pré-sal) e otimização de processos de refino.   
Subdomínio Principal: Exploração e Extração em Águas Profundas e Pré-Sal.  

**-Nubank**
Diferencial Competitivo: Isenção de tarifas em serviços financeiros tradicionais aliada a uma experiência de usuário simplificada, 100% digital e transparente via aplicativo.   
Subdomínio Principal: Plataforma Digital de Serviços Financeiros e Concessão de Crédito Descomplicada.   

**-Tesla**
Diferencial Competitivo: Tecnologia de baterias de alta eficiência, ecossistema de software veicular integrado com condução autônoma (FSD) e arquitetura inovadora de veículos elétricos.   
Subdomínio Principal: Engenharia de Veículos Elétricos e Algoritmos de Condução Autônoma.   

**-Netflix**
Diferencial Competitivo: Algoritmo avançado de recomendação personalizada de conteúdo, infraestrutura global otimizada de streaming de alta disponibilidade e produção contínua de conteúdos originais de grande apelo.   Subdomínio Principal: Motor de Recomendação e Distribuição/Streaming Personalizado de Mídia.

---

## Questão 2 - Atividade:: Identificar e Classificar Subdomínios

**Enunciado:**
> 1. Identifique o domínio de negócios da Gigmaster.
 
**Resolução:**

Venda e distribuição de ingressos para shows e eventos.

---


**Enunciado:**
>2. Identifique e classifique os subdomínios associados, justificando.

**Resolução:**

Recomendação e Análise de Preferências Musicais com Privacidade (Subdomínio Principal): É o grande diferencial competitivo da empresa. Consiste no algoritmo que analisa bibliotecas musicais, streaming e redes sociais trabalhando exclusivamente com dados anônimos para proteger a privacidade dos usuários. Possui alta complexidade e alta volatilidade por demandar inovação contínua.   

Segurança e Criptografia de Dados (Subdomínio Genérico): Responsável por criptografar todas as informações pessoais dos usuários. É um problema complexo, porém padronizado, com soluções de mercado já testadas e aprovadas.   

Registro de Histórico de Shows Passados (Subdomínio de Suporte): Módulo complementar que permite ao usuário cadastrar shows que frequentou anteriormente (mesmo comprados fora da plataforma) para alimentar o motor de recomendações. Trata-se de uma funcionalidade necessária de baixa complexidade (estilo CRUD) e sem diferencial competitivo próprio.   

Venda e Processamento de Ingressos / Pagamentos (Subdomínio Genérico): O fluxo tradicional de vendas e pagamentos de ingressos, por ser uma atividade padronizada no mercado. 


---


**Enunciado:**
>3. Quais decisões de design podem ser consideradas?

**Resolução:**
Subdomínio Principal (Recomendação Anônima): Deve ser desenvolvido internamente pela própria equipe da Gigmaster com foco total de arquitetura, investimento e prioridade técnica.  

Subdomínios Genéricos (Criptografia e Pagamentos): Devem ser resolvidos adotando bibliotecas consolidadas, APIs de terceiros ou componentes de software abertos/prontos de prateleira, sem reinvenção de roda. 

Subdomínio de Suporte (Histórico de Shows): Pode ser desenvolvido internamente com uma arquitetura bem simples (como um cadastro/CRUD direto) ou até terceirizado. 


---


## Questão 3 - Atividade:: Identificar e Classificar Subdomínios (2)

**Enunciado:**
> 1. Identifique o domínio de negócios da BusVNext.

**Resolução:**

Transporte público de passageiros por ônibus sob demanda (modelo estilo táxi/viagens personalizadas).

---

**Enunciado:**
> 2. Identifique e classifique os subdomínios associados,justificando

**Resolução:**

Otimização e Roteamento de Ônibus em Tempo Real (Subdomínio Principal): É a base da vantagem competitiva da empresa. Resolve uma variação complexa do problema do caixeiro-viajante ao ajustar dinamicamente as rotas dos ônibus para buscar passageiros no horário correto e priorizar partidas rápidas. É de altíssima complexidade e está em contínua evolução/ajuste (alta volatilidade).   

Monitoramento de Trânsito e Alertas em Tempo Real (Subdomínio Genérico): Dados sobre condições de tráfego que alimentam o roteador. Trata-se de um problema complexo, mas resolvido de forma padronizada no mercado por provedores especializados.   

Gestão de Promoções e Descontos Especiais (Subdomínio de Suporte): Sistema para oferecer descontos que atram clientes e equilibrem a demanda entre horários de pico e fora de pico. É uma funcionalidade necessária para a estratégia comercial, porém de baixa complexidade técnica e sem diferencial competitivo direto no serviço de transporte em si.   

Agendamento/Solicitação de Viagens via App (Subdomínio de Suporte ou Genérico): Interface para o cliente solicitar e marcar a partida pelo celular, servindo de apoio para a entrada de dados do sistema principal.  


---

>3. Quais decisões de design podem ser consideradas?

**Resolução:**

Subdomínio Principal (Roteamento Dinâmico): Deve ser estritamente desenvolvido dentro da empresa (in-house), recebendo prioridade total de engenharia por se tratar do coração do negócio.   

Subdomínio Genérico (Trânsito e Alertas): Deve ser adotado via integração (APIs) com provedores terceirizados já consolidados no mercado, evitando custos de desenvolvimento interno para um problema já resolvido.  

Subdomínio de Suporte (Gestão de Promoções/Descontos): Pode ser desenvolvido internamente de forma simples ou terceirizado/construído com regras diretas e estáveis.  

---