# Dicionário de Dados Técnico - Telecom X

| Índice | Nome Original            | Nome Transformado         | Descrição                                      | Codificação                                                                 | Tipo    | Não Nulos | Valores Únicos | Cardinalidade |
|--------|--------------------------|---------------------------|-----------------------------------------------|-----------------------------------------------------------------------------|---------|-----------|----------------|---------------|
| 0      | `customerID`             | `customer_id`             | Identificador único do cliente                | Alfanumérico                                                               | `object`| 7,032     | 7,032          | Alta          |
| 1      | `Churn`                  | `target_churn`            | Churn (cancelamento)                         | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 2      | `customer_gender`        | `gender`                  | Gênero do cliente                            | `Male`<br>`Female`                                                         | `object`| 7,032     | 2              | Baixa         |
| 3      | `customer_SeniorCitizen` | `is_elderly`              | Cliente idoso (65+ anos)                     | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 4      | `customer_Partner`       | `has_partner`             | Possui parceiro(a)                           | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 5      | `customer_Dependents`    | `has_dependents`          | Possui dependentes                           | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 6      | `customer_tenure`        | `tenure_months`           | Tempo de permanência (meses)                 | Valor numérico (1-72)                                                      | `int64` | 7,032     | 72             | Média         |
| 7      | `phone_PhoneService`     | `has_phone_service`       | Possui serviço telefônico                    | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 8      | `phone_MultipleLines`    | `has_multiple_lines`      | Possui múltiplas linhas                      | `0` = Sem serviço<br>`1` = Não<br>`2` = Sim                                | `int64` | 7,032     | 3              | Baixa         |
| 9      | `internet_InternetService` | `internet_service_type` | Tipo de serviço de internet                 | `0` = Sem internet<br>`1` = DSL<br>`2` = Fibra Ótica                       | `int64` | 7,032     | 3              | Baixa         |
| 10     | `internet_OnlineSecurity` | `has_online_security`    | Possui segurança online                      | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 11     | `internet_OnlineBackup`   | `has_online_backup`      | Possui backup online                         | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 12     | `internet_DeviceProtection` | `has_device_protection` | Possui proteção de dispositivo               | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 13     | `internet_TechSupport`    | `has_tech_support`       | Possui suporte técnico                       | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 14     | `internet_StreamingTV`    | `uses_streaming_tv`      | Utiliza streaming de TV                      | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 15     | `internet_StreamingMovies` | `uses_streaming_movies`  | Utiliza streaming de filmes                  | `0` = Sem internet<br>`1` = Não<br>`2` = Sim                               | `int64` | 7,032     | 3              | Baixa         |
| 16     | `account_Contract`        | `contract_term_months`   | Tipo de contrato                             | `0` = Mensal<br>`1` = Anual<br>`2` = Bienal                                | `int64` | 7,032     | 3              | Baixa         |
| 17     | `account_PaperlessBilling` | `uses_paperless_billing` | Utiliza fatura digital                       | `0` = Não<br>`1` = Sim                                                     | `int64` | 7,032     | 2              | Baixa         |
| 18     | `account_PaymentMethod`   | `payment_method_type`    | Método de pagamento                          | `0` = Cheque correio<br>`1` = Cheque eletrônico<br>`2` = Transferência<br>`3` = Cartão | `int64` | 7,032 | 4 | Baixa |
| 19     | `account_Charges_Daily`   | `daily_charges`          | Gastos diários                          | Valor numérico (0.00 - 100.00)                                             | `float64` | 7,032  | 321           | Alta          |
| 20     | `account_Charges_Monthly` | `monthly_charges`        | Gastos mensais                          | Valor numérico (0.00 - 200.00)                                             | `float64` | 7,032  | 1,584         | Alta          |
| 21     | `account_Charges_Total`   | `total_charges`          | Gastos totais acumulados                | Valor numérico (0.00 - 10,000.00)                                          | `float64` | 7,032  | 6,530         | Alta          |

### Convenções:
- **Cardinalidade**: 
  - `Alta` > 100 valores únicos
  - `Média` = 10-100 valores
  - `Baixa` < 10 valores
- **Tipos**: 
  - `object`: Strings/categóricos
  - `int64`: Inteiros
  - `float64`: Decimais