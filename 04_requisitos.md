Requisitos do Sistema

1. Introdução

Este documento tem como objetivo especificar de forma clara, estruturada e verificável os requisitos do sistema de agendamento. Os requisitos aqui descritos representam as necessidades funcionais e não funcionais identificadas a partir do contexto do problema, do escopo definido e das expectativas dos stakeholders. Este documento serve como base para a definição da arquitetura do sistema, regras de negócio, critérios de validação, testes e futuras evoluções, garantindo rastreabilidade e redução de ambiguidades durante o ciclo de vida do software.

2. Requisitos Funcionais

Os requisitos funcionais descrevem o que o sistema deve fazer, independentemente da tecnologia utilizada para sua implementação.

RF01 — Gerenciamento de Usuários Administrativos

O sistema deve permitir o cadastro, edição, ativação e desativação de usuários administrativos, possibilitando o controle de acesso às funcionalidades do sistema.

RF02 — Autenticação e Controle de Acesso

O sistema deve permitir que usuários administrativos realizem autenticação por meio de credenciais válidas, garantindo que apenas usuários autorizados tenham acesso às funcionalidades internas.

RF03 — Criação de Agendamentos

O sistema deve permitir a criação de agendamentos contendo, no mínimo, data, horário, responsável pelo atendimento e status inicial do agendamento.

RF04 — Alteração de Agendamentos

O sistema deve permitir a alteração de agendamentos previamente cadastrados, respeitando as regras de disponibilidade e evitando conflitos de horário.

RF05 — Cancelamento de Agendamentos

O sistema deve permitir o cancelamento de agendamentos, mantendo o histórico da operação para fins de controle e auditoria.

RF06 — Consulta de Agenda

O sistema deve permitir a visualização da agenda por dia, semana ou período personalizado, facilitando o acompanhamento operacional dos atendimentos.

RF07 — Controle de Disponibilidade

O sistema deve impedir a criação de agendamentos em horários indisponíveis ou já ocupados, garantindo a integridade da agenda.

3. Requisitos Não Funcionais

Os requisitos não funcionais definem como o sistema deve se comportar, estabelecendo atributos de qualidade essenciais para a operação, manutenção e segurança da solução.

RNF01 — Desempenho

O sistema deve responder às operações principais (criação, alteração e consulta de agendamentos) em até 2 segundos sob condições normais de uso.

RNF02 — Disponibilidade

O sistema deve apresentar disponibilidade mínima de 99% no período mensal, considerando janelas programadas de manutenção.

RNF03 — Segurança da Informação

O sistema deve garantir a proteção dos dados armazenados, utilizando mecanismos de autenticação, autorização e controle de acesso adequados ao perfil dos usuários.

RNF04 — Usabilidade

O sistema deve possuir interface intuitiva e consistente, permitindo que usuários realizem as principais operações com esforço cognitivo reduzido e sem necessidade de treinamento avançado.

RNF05 — Manutenibilidade

O sistema deve ser estruturado de forma modular, facilitando correções, evoluções e adaptações futuras sem impacto significativo nas funcionalidades existentes.

RNF06 — Compatibilidade

O sistema deve ser compatível com os principais navegadores modernos, garantindo acesso uniforme aos usuários finais.

RNF07 — Escalabilidade

O sistema deve permitir crescimento gradual no volume de agendamentos e usuários sem degradação significativa de desempenho.

4. Restrições e Premissas
Restrições

O sistema será disponibilizado inicialmente como aplicação web.

Não haverá, nesta fase, integração com sistemas externos ou meios de pagamento.

O suporte a múltiplos idiomas não faz parte da versão inicial.

Premissas

Os usuários administrativos possuem conhecimento básico de operação em sistemas web.

O ambiente de operação inicial será de pequeno a médio porte.

O idioma padrão do sistema será o português.
