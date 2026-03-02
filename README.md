# 📊 Inteligência de Vendas e Sistema de Relatórios Automatizados

Este projeto automatiza o fluxo de consolidação de dados, estruturação em banco de dados relacional e distribuição de relatórios personalizados, simulando um cenário real de Engenharia de Dados e BI para o varejo.

## 📌 1. O Problema de Negócio
A consolidação manual de dados de vendas em múltiplas unidades é lenta e sujeita a erros. O tempo gasto para gerar métricas e enviar relatórios individuais atrasa a tomada de decisão estratégica.

**O Desafio:** Criar uma solução escalável que processe milhares de registros, garanta a integridade dos dados via SQL e entregue KPIs críticos automaticamente e com segurança.

## 🛠️ 2. Decisões Técnicas & Stack
A arquitetura da solução foca em **governança** e **rastreabilidade**:

* **Python & Pandas:** Motor de ETL para processamento e transformação de bases volumosas.
* **SQL (SQLite) & SQLAlchemy:** Migração de dados estáticos para um banco de dados relacional, garantindo persistência e integridade.
* **SQL Views:** Implementação da `vw_insights_vendas` para processar cálculos complexos (como Ticket Médio) diretamente no banco, otimizando a performance.
* **Sistema de Logging:** Implementação de rastreabilidade total do pipeline, registrando sucessos e falhas em um arquivo `.log` para auditoria.
* **Integração SMTP (Smtplib):** Envio automatizado de e-mails em HTML profissional.
* **Segurança (Secrets):** Uso de variáveis de ambiente e Senhas de App para proteção de credenciais.

## 🚀 3. Desafios de Engenharia & Impacto
O projeto foi elevado ao nível de solução corporativa:

* **Escalabilidade e Performance:** O uso de **Views SQL** permite que ferramentas externas consumam dados já agregados, reduzindo o consumo de memória.
* **Rastreabilidade (Observabilidade):** Com o sistema de **Logger**, o pipeline comunica exatamente onde e por que um erro ocorreu, facilitando a manutenção.
* **KPIs Automatizados via SQL:**
    * **Faturamento Total:** Consolidado por unidade.
    * **Ticket Médio:** Calculado nativamente no banco de dados.
    * **Volume de Pedidos:** Contagem única de transações por loja.

## 🔍 4. Perguntas de Negócio Respondidas
* *Qual unidade possui a melhor eficiência de venda (Ticket Médio)?*
* *Como garantir a integridade dos dados históricos através de um banco de dados?*
* *Como monitorar falhas no processo de automação sem precisar revisar o código manualmente?*

---
**Desenvolvido por Guilherme Rodrigues** [LinkedIn](https://www.linkedin.com/in/guilherme584rodrigues/) | [GitHub](https://github.com/GLRodrigues58)
