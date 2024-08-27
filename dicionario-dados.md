### Dicionário de Dados - Workshop Data Science

#### Tabela: cliente
| Campo           | Tipo          | Descrição                                                                                  |
|-----------------|---------------|--------------------------------------------------------------------------------------------|
| `idCliente`     | String        | Identificador único do cliente.        |
| `nrPontosCliente` | Bigint      | Número de pontos acumulados pelo cliente.                                   |
| `flEmailCliente` | Bigint       | Indicador se o cliente cadastrou seu e-mail.     |

#### Tabela: transacoes
| Campo             | Tipo      | Descrição                                                                                                 |
|-------------------|-----------|-----------------------------------------------------------------------------------------------------------|
| `idTransacao`     | String    | Identificador único da transação.                                             |
| `idCliente`       | String    | Identificador único do cliente.  |
| `dtTransacao`     | String  | Data e hora da transação.                                |
| `nrPontosTransacao` | Bigint | Número de pontos atribuídos ou retirados ao cliente na transação.  |

#### Tabela: transacao_produto
| Campo                 | Tipo      | Descrição                                                                                                 |
|-----------------------|-----------|-----------------------------------------------------------------------------------------------------------|
| `idTransacaoProduto`  | String    | Identificador único da transação-produto.                                         |
| `idTransacao`         | String    | Identificador único da transação associada.                         |
| `descNomeProduto`     | String    | Descrição do produto adquirido na transação.                       |
| `nrQuantidadeProduto` | Bigint   | Quantidade de unidades do produto adquiridas na transação.   |
