# User Stories

## EP-01 - Formatação de Edital

### US-01 - Gerar edital automaticamente

Como servidor responsável pela licitação,
quero gerar automaticamente o edital a partir do TR e do Mapa de Riscos,
para reduzir erros manuais na elaboração do documento.

Critérios de Aceite:

Cenário 1: Geração bem-sucedida
  Dado que o TR e o Mapa de Riscos foram recebidos
  Quando solicito a geração do edital
  Então o sistema cria o edital no formato oficial
  E associa os documentos recebidos ao edital

Estimativa: M
Prioridade: Alta

---

### US-02 - Visualizar edital formatado

Como servidor responsável pela licitação,
quero visualizar o edital formatado antes do envio,
para conferir se as informações estão corretas.

Critérios de Aceite:

Cenário 1: Visualização disponível
  Dado que o edital foi gerado
  Quando acesso a tela de visualização
  Então o sistema exibe o documento completo para conferência

Estimativa: S
Prioridade: Alta

---

## EP-03 - Validação de Completude

### US-03 - Validar documentos obrigatórios

Como servidor responsável pela licitação,
quero validar a presença dos documentos obrigatórios,
para evitar o envio de editais incompletos.

Critérios de Aceite:

Cenário 1: Todos os documentos presentes
  Dado que o edital possui todos os anexos obrigatórios
  Quando realizo a validação
  Então o sistema informa que o edital está apto para envio

Cenário 2: Documento ausente
  Dado que existe um anexo obrigatório ausente
  Quando realizo a validação
  Então o sistema informa qual documento está faltando
  E bloqueia o envio

Estimativa: M
Prioridade: Alta

---

## EP-04 - Envio para Prefeitura

### US-04 - Enviar edital para Prefeitura

Como servidor responsável pela licitação,
quero enviar o edital para a Prefeitura,
para que ela conduza o pregão eletrônico.

Critérios de Aceite:

Cenário 1: Envio realizado
  Dado que o edital foi validado
  Quando aciono a opção de envio
  Então o sistema encaminha o edital à Prefeitura
  E registra a confirmação do envio

Estimativa: L
Prioridade: Alta

---

## EP-05 - Auditoria

### US-05 - Registrar histórico de envio

Como auditor do sistema,
quero consultar o histórico de envios dos editais,
para garantir rastreabilidade das ações realizadas.

Critérios de Aceite:

Cenário 1: Consulta de histórico
  Dado que houve envios registrados
  Quando acesso o histórico
  Então o sistema exibe usuário, data, horário e status do envio

Estimativa: S
Prioridade: Média