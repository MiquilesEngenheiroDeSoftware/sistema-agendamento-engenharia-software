Introdução

Este documento define as regras de negócio que governam o funcionamento do sistema de agendamento. As regras aqui descritas representam restrições fundamentais do domínio, sendo independentes de tecnologia, interface ou decisão de implementação. Seu objetivo é garantir consistência operacional, integridade dos dados, rastreabilidade das operações e previsibilidade do comportamento do sistema, servindo como referência para arquitetura, desenvolvimento, testes, auditoria e evolução futura.

RN01 — Exclusividade Temporal de Agendamentos

O sistema deve garantir que não exista mais de um agendamento ativo para o mesmo responsável em um mesmo intervalo de data e horário, prevenindo conflitos operacionais e sobreposição de atendimentos.

RN02 — Ciclo de Vida do Agendamento

Todo agendamento deve obrigatoriamente seguir um ciclo de vida previamente definido, podendo assumir apenas estados válidos e controlados pelo sistema (ex.: agendado, realizado, cancelado), sendo vedada a criação de estados arbitrários.

RN03 — Imutabilidade de Registros Históricos

Agendamentos com status finalizado ou cancelado não podem ser removidos do sistema, garantindo a preservação do histórico para fins de auditoria, rastreabilidade e análise gerencial.

RN04 — Restrições de Alteração

Agendamentos com status realizado não podem sofrer alterações, assegurando a integridade dos dados históricos e evitando inconsistências retroativas.

RN05 — Governança da Disponibilidade

A disponibilidade de horários deve ser definida e controlada previamente pelo sistema, sendo proibida a criação de agendamentos fora das janelas de atendimento configuradas.

RN06 — Controle de Autoridade

Somente usuários devidamente autorizados, conforme seu perfil de acesso, podem executar operações críticas como criação, alteração ou cancelamento de agendamentos.

RN07 — Rastreabilidade Operacional

Toda operação relevante realizada no sistema deve ser registrada, permitindo a identificação do usuário responsável, data, horário e tipo de ação executada.

RN08 — Validação Temporal

O sistema deve impedir o registro de agendamentos em datas ou horários anteriores ao momento atual, prevenindo inconsistências temporais.

RN09 — Consistência de Responsabilidades

Todo agendamento deve estar vinculado a um responsável válido e ativo no sistema, sendo vedada a associação a entidades inexistentes ou inativas.

RN10 — Preservação de Consistência de Dados

Alterações em agendamentos devem preservar a integridade dos dados relacionados, garantindo que mudanças não provoquem estados inconsistentes no sistema.

RN11 — Limitação Operacional Configurável

O sistema deve permitir a definição de limites operacionais, como quantidade máxima de agendamentos por responsável em um determinado período, visando controle de carga e qualidade do atendimento.

RN12 — Auditoria e Conformidade

O sistema deve possibilitar auditoria completa das operações críticas, atendendo requisitos de governança, conformidade e prestação de contas.

RN13 — Validação de Jornada de Atendimento

Agendamentos devem respeitar rigorosamente a jornada de atendimento configurada, incluindo horários de início, término e intervalos.

RN14 — Impacto na Disponibilidade

Somente agendamentos com status ativo devem impactar diretamente a disponibilidade de horários, garantindo previsibilidade no controle da agenda.

RN15 — Independência de Interface

As regras de negócio devem ser aplicadas independentemente da interface de acesso, garantindo comportamento consistente do sistema em qualquer ponto de uso.
