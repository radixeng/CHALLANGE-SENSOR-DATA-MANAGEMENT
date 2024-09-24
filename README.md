# Desafio Radix

Você é um desenvolvedor em uma grande empresa do setor de óleo e gás. Uma das plantas dessa empresa instalou sensores em seus 2.000 equipamentos, e você foi encarregado de criar a infraestrutura para receber os dados desses sensores em tempo real.

## Descrição

Os equipamentos são capazes de enviar dados no formato JSON para um endpoint. Um exemplo do payload é:

```json
{
  "equipmentId": "EQ-12495",
  "timestamp": "2023-02-15T01:30:00.000-05:00",
  "value": 78.42
}
```

- `equipmentId`: o identificador do equipamento;
- `timestamp`: a data e hora em que o evento ocorreu, incluindo o fuso horário;
- `value`: o valor do sensor com precisão de duas casas decimais.

## Tarefas

### Modelagem de Banco de Dados
Modele um banco de dados da sua escolha para o caso de uso apresentado.

### Criação de API
Crie uma API com um endpoint que receba as requisições em tempo real e armazene os dados no banco de dados.

### Lidar com Falhas Técnicas
Alguns dos sensores da planta podem apresentar falhas técnicas, resultando em lacunas nos dados. Para lidar com isso, o fornecedor pode enviar arquivos CSV com os dados perdidos.  
Adicione na API um endpoint que receba um arquivo CSV, faça o parser dos dados e salve os valores no banco de dados. O formato do CSV pode ser encontrado na tabela abaixo:


| equipmentId | timestamp                      | value |
|-------------|---------------------------------|-------|
| EQ-12495    | 2023-02-12T01:30:00.000-05:00   | 78.8  |
| EQ-12492    | 2023-01-12T01:30:00.000-05:00   | 8.8   |


### Visualização de Dados
Crie uma tela que exiba o valor médio de cada sensor nas últimas 24 horas, 48 horas, 1 semana ou 1 mês.
Sua tela deve conter gráficos para facilitar a análise.

### Documentação
Crie uma documentação detalhada da sua solução.

