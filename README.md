# Manual Quality Assurance — Sauce Demo E-commerce

Este repositório apresenta o ciclo completo de testes funcionais manuais executados na plataforma de e-commerce Sauce Demo. O projeto demonstra a aplicação prática de técnicas de mapeamento de cenários, engenharia de testes, análise de riscos operacionais e documentação técnica de defeitos.

O relatório executivo formal emitido para os stakeholders pode ser acessado diretamente na pasta [/docs/Relatório de Execução de Testes.pdf](./docs/Relatório%20de%20Execução%20de%20Testes.pdf).

## Contexto e Escopo
O objetivo principal foi validar a integridade dos fluxos críticos de negócios da aplicação através da simulação da jornada real do usuário.

* **Ambiente de Testes:** Windows 11 | Navegador Brave (Base Chromium)
* **Plataforma Alvo:** [Sauce Demo Shopify](https://sauce-demo.myshopify.com/)
* **Módulos Avaliados:** Login, Carrinho de Compras, Checkout e Gateway de Pagamento

## Engenharia de Testes Aplicada
Para garantir a cobertura sem redundância, foram utilizadas as seguintes técnicas de design de teste:
* **Análise de Valor Limite (BVA):** Validação de campos de input no checkout (CEP, número de cartão).
* **Particionamento de Equivalência (EP):** Divisão de fluxos de login válidos/inválidos e regras de cupom de desconto.
* **Testes Baseados em Riscos:** Priorização de execução focada no Gateway de Pagamento.

## Resumo da Execução (Status do Projeto)
Resultados obtidos a partir da execução de 20 casos de teste
| Critério de Aceitação | Meta | Atingido | Status |
| :--- | :---: | :---: | :---: |
| Taxa de Aprovação | $\ge$ 95% | **95%** | Passou |
| Bugs Críticos/Altos Abertos | 0 | **0** | Passou |
| Fluxos Principais Operacionais | 100% | **100%** | Passou |

> **Nota sobre Defeitos:** Foi identificado 1 defeito de severidade Média (BUG-001: Falha na validação geográfica de frete internacional), já documentado e reportado para a equipe de desenvolvimento.

## Arquitetura do Repositório
```text
├── [docs/](./docs/)
│   └── [Relatório de Execução de Testes.pdf](./docs/Relatório%20de%20Execução%20de%20Testes.pdf)  # Relatório oficial para stakeholders
├── [evidences/](./evidences/)
│   ├── [bug_001_reproducao.png](./evidences/bug_001_reproducao.png)                               # Evidência visual da falha geográfica
│   ├── [checkout_fluxo.png](./evidences/checkout_fluxo.png)                                       # Mapeamento do Checkout
│   ├── [login_sucesso.png](./evidences/login_sucesso.png)                                         # Autenticação de usuário
│   └── [produto_carrinho.png](./evidences/produto_carrinho.png)                                   # Estado e persistência do carrinho
└── README.md
