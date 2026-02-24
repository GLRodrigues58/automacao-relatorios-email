# 📊 Inteligência de vendas e sistema de relatórios automatizados

Este projeto automatiza o fluxo de consolidação de dados, cálculo de KPIs e distribuição de relatórios personalizados por e-mail, simulando um cenário real de BI (Business Intelligence) para uma rede de varejo multiloja.

## 📌 1. O Problema de Negócio
Em operações de varejo com múltiplas unidades, a consolidação manual de dados de vendas é um processo lento e propenso a falhas. O tempo gasto por analistas para gerar métricas e enviar relatórios individuais para cada gerente atrasa a tomada de decisão estratégica.

**O Desafio:** Criar uma solução escalável que processe milhares de registros e garanta a entrega de KPIs críticos diretamente aos responsáveis (Gerentes e Diretores) de forma automática e segura.

## 🛠️ 2. Decisões Técnicas & Stack
A arquitetura da solução foca em **robustez** e **autonomia**:

* **Python & Pandas:** Utilizados para o motor de ETL (Extração, Transformação e Carga), permitindo o processamento eficiente de bases de dados volumosas.
* **Agrupamento Dinâmico:** Implementação de lógica de agrupamento (`.groupby`) para segmentar KPIs por unidade de negócio (ID Loja).
* **Integração SMTP (Smtplib):** Automação do envio de e-mails com suporte a corpo de mensagem em HTML, garantindo uma apresentação visual profissional e acessível para dispositivos móveis.
* **Segurança de Credenciais:** Uso de variáveis de ambiente para gerenciamento de tokens e senhas de e-mail, seguindo boas práticas de segurança de software.

## 🚀 3. Desafios de Engenharia & Impacto
O projeto foi estruturado para ser entregue como uma solução corporativa:

* **Escalabilidade:** O script processa e distribui dados para 25 lojas em questão de segundos, uma tarefa que levaria horas se feita manualmente.
* **KPIs Automatizados:**
    * **Faturamento Total:** Visão macro da performance financeira.
    * **Diversidade de Produtos:** Monitoramento da variedade vendida por unidade.
    * **Ticket Médio:** Indicador chave de eficiência de vendas por cliente.
* **Visão Executiva:** Além dos envios individuais, o sistema gera um "One Page Report" consolidado para a diretoria com o ranking de performance das unidades.

## 🔍 4. Perguntas de Negócio Respondidas
* *Qual unidade possui a melhor eficiência de venda (Ticket Médio)?*
* *Quais lojas atingiram o volume de vendas esperado?*
* *Como garantir que a informação chegue ao tomador de decisão sem intervenção humana diária?*

## 🔮 O que eu faria diferente? (Próximos Passos)
1.  **Persistência em SQL:** Migrar a base de arquivos estáticos (`.xlsx`) para um banco de dados relacional (PostgreSQL/SQLite) para maior integridade dos dados.
2.  **Visualização:** Conectar o output a um dashboard no Power BI/Tableau para análise de tendências históricas.
3.  **Monitoramento:** Implementar logs de envio para garantir o rastreio de possíveis falhas na rede de e-mails.

## 🚀 Como executar

```bash
pip install -r requirements.txt
```
---
Desenvolvido por **Guilherme Rodrigues**
