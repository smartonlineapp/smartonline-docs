# Adicionar Pedido

> **POST** https://api.smartonline.app/api/PedidoCompraExterno/adicionar

## Payload

### PedidoCompra

| **Propriedade**   | **Tipo**      | **Descrição**                                                          |
| ----------------- | ------------- | ---------------------------------------------------------------------- |
| NumeroPedido      | int32         | O número do pedido                                                     |
| DataPedido        | datetime      | Data do pedido                                                         |
| TipoPedido        | string        | O tipo do pedido.<br>**Valores possíveis:**<br>- Revenda <br>- Entrada |
| Emergencial       | boolean       | Mostra se o pedido é emergencial                                       |
| EmpresaCompradora | EmpresaPedido | Dados da empresa compradora do pedido                                  |

### EmpresaPedido

| **Propriedade**   | **Tipo** | **Descrição**                                                                       |
| ----------------- | -------- | ----------------------------------------------------------------------------------- |
| Cnpj              | string   | CNPJ da empresa.<br> Obs: **_Enviar sem máscara_**                                  |
| RazaoSocial       | string   | Razão social da empresa                                                             |
| NomeFantasia      | string   | Nome fantasia da empresa                                                            |
| InscricaoEstadual | string   | Inscrição estadual da empresa<br>Caso a empresa não tenha, enviar "" (string vazia) |
| Cep               | string   | CEP da empresa<br> Obs: **_Enviar sem máscara_**                                    |

### Exemplo

<details>
<summary>Clique aqui para expandir.</summary>

```json
{
  "NumeroPedido": 1,
  "DataPedido": "2021-03-22 00:00-03:00",
  "TipoPedido": "Revenda",
  "Emergencial": false,
  "CondicaoPagamento": "60 DDL",
  "PercentualFrete": 0,
  "PercentualCustoFinanceiro": 0,
  "Observacao": "Este pedido é um payload de exemplo",
  "DescricaoRegimeEspecial": "Esta descrição também é um exemplo",
  "QuantidadeItens": 1,
  "ValorTotalPedido": 199.0,
  "Coleta": false,
  "PedidoProgramado": false,
  "EmailNFe": "nfe@onlineapp.com.br",
  "EmpresaCompradora": {
    "Cnpj": "99999999999999",
    "RazaoSocial": "Online Applications",
    "NomeFantasia": "Online Applications",
    "InscricaoEstadual": "99999999999",
    "Cep": " 13080650",
    "Logradouro": "Av. José Rocha Bonfim",
    "Numero": "214",
    "Complemento": "BL Madri, SL 236",
    "Bairro": "Lot. Center Santa Genebra",
    "Municipio": "Campinas",
    "Estado": "SP",
    "Pais": "Brasil"
  },
  "EmpresaCobranca": {
    "Cnpj": "99999999999999",
    "RazaoSocial": "Online Applications",
    "NomeFantasia": "Online Applications",
    "InscricaoEstadual": "99999999999",
    "Cep": " 13080650",
    "Logradouro": "Av. José Rocha Bonfim",
    "Numero": "214",
    "Complemento": "BL Madri, SL 236",
    "Bairro": "Lot. Center Santa Genebra",
    "Municipio": "Campinas",
    "Estado": "SP",
    "Pais": "Brasil"
  },
  "EmpresaEntrega": {
    "Cnpj": "99999999999999",
    "RazaoSocial": "Online Applications",
    "NomeFantasia": "Online Applications",
    "InscricaoEstadual": "99999999999",
    "Cep": " 13080650",
    "Logradouro": "Av. José Rocha Bonfim",
    "Numero": "214",
    "Complemento": "BL Madri, SL 236",
    "Bairro": "Lot. Center Santa Genebra",
    "Municipio": "Campinas",
    "Estado": "SP",
    "Pais": "Brasil"
  },
  "Fornecedor": {
    "Cnpj": "99999999999999",
    "RazaoSocial": "Online Applications",
    "NomeFantasia": "Online Applications",
    "InscricaoEstadual": "99999999999",
    "Cep": " 13080650",
    "Logradouro": "Av. José Rocha Bonfim",
    "Numero": "214",
    "Complemento": "BL Madri, SL 236",
    "Bairro": "Lot. Center Santa Genebra",
    "Municipio": "Campinas",
    "Estado": "SP",
    "Pais": "Brasil"
  },
  "Comprador": {
    "Nome": "Elias Rodrigues",
    "Email": "elias@onlineapp.com.br",
    "Telefone": "1940628611",
    "Celular": "99999999999"
  },
  "Negociador": {
    "Nome": "Elias Rodrigues",
    "Email": "elias@onlineapp.com.br",
    "Telefone": "1940628611",
    "Celular": "99999999999"
  },
  "AnalistaFollowUp": {
    "Nome": "Elias Rodrigues",
    "Email": "elias@onlineapp.com.br",
    "Telefone": "1940628611",
    "Celular": "99999999999"
  },
  "Vendedor": {
    "Nome": "Elias Rodrigues",
    "Email": "elias@onlineapp.com.br",
    "Telefone": "1940628611",
    "Celular": "99999999999"
  },
  "Itens": [
    {
      "Item": 1,
      "CodigoProduto": "201474",
      "DescricaoProduto": "CABO MT 12/20KV 105G EPR 120MM PT",
      "DescricaoTecnicaProduto": "CABO MT 12/20KV 105G EPR 120MM PT",
      "ReferenciaProdutoFabricante": "26564268",
      "CodigoProdutoFabricante": "26564268",
      "Ean": ["1324689753217"],
      "UnidadeMedida": "MT",
      "QuantidadePedida": 10.0,
      "QuantidadeRecebida": 10.0,
      "QuantidadePercentualAcima": 10.0,
      "QuantidadeLimiteAcima": 10.0,
      "PrecoBruto": 1.99,
      "PercentualDesconto": 0,
      "PercentualDiferencaIcms": 0,
      "PrecoLiquido": 0.0,
      "PrecoLiquidoPercentualAcima": 10.0,
      "PrecoLiquidoPercentualAbaixo": 10.0,
      "PrecoLiquidoLimiteAcima": 10.0,
      "PrecoLiquidoLimiteAbaixo": 10.0,
      "ValorTotal": 1.99,
      "AliquotaIcms": 0.0,
      "AliquotaIpi": 0.0,
      "Ncm": "8544.60.00",
      "PrazoMaximoEntrega": "2021-03-22 00:00-03:00"
    }
  ]
}
```

</details>

## Response

| **Propriedade**   | **Tipo** | **Descrição**                                                                              |
| ----------------- | -------- | ------------------------------------------------------------------------------------------ |
| ChavePedido       | string   | O identificador do pedido no Smart Online. <br> Ele será utilizado em futuras requisições. |
| DataProcessamento | datetime | A data em que o pedido foi processado.                                                     |

### Exemplo

<details>
<summary>Clique aqui para expandir.</summary>

```json
{
  "ChavePedido": "1202011201714506990438",
  "DataProcessamento": "2020-11-20T17:14:50.6990423-03:00"
}
```

</details>
