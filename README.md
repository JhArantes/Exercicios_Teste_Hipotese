# 🏥 Testes de Hipótese em Dados de Saúde

Este repositório contém uma coleção de exercícios práticos e resolvidos sobre **Testes de Hipótese** aplicados ao contexto da Saúde. O objetivo é demonstrar a aplicação estatística para validar suposições clínicas, eficácia de tratamentos e análise de indicadores populacionais utilizando Python e a biblioteca `scipy`.

---

## 📊 O que este projeto cobre?

O foco principal é a tomada de decisão estatística baseada em diferentes cenários de amostragem e direções de teste.

### 1. Tipos de Testes Implementados
* **Uma Amostra (One-sample):** Comparação de uma média amostral contra um valor populacional conhecido (ex: A média de IMC desta clínica é diferente da média nacional?).
* **Duas Amostras Independentes:** Comparação entre dois grupos distintos (ex: Grupo Controle vs. Grupo Tratamento).
* **Amostras Pareadas (Paired Samples):** Comparação de medidas no mesmo indivíduo em tempos diferentes (ex: Pressão arterial antes e depois do medicamento).

### 2. Direções da Hipótese Alternativa ($H_1$)
Configuramos o parâmetro `alternative` no `scipy` para três direções:
* `two-sided` (Bilateral): Verifica qualquer diferença.
* `larger` (Unicaudal à direita): Verifica se o efeito aumentou.
* `smaller` (Unicaudal à esquerda): Verifica se o efeito diminuiu.

---

## 🛠️ Tecnologias Utilizadas

* **Python 3.x**
* **Pandas**: Manipulação de dados biométricos.
* **SciPy**: Cálculo P valor.

---

## 📈 Resumo Visual das Hipóteses

| Teste | Hipótese Alternativa ($H_1$) | Parâmetro `alternative` |
| :--- | :--- | :--- |
| **Bilateral** | $\mu \neq \mu_0$ | `'two-sided'` |
| **Unicaudal à Esquerda** | $\mu < \mu_0$ | `'smaller'` |
| **Unicaudal à Direita** | $\mu > \mu_0$ | `'larger'` |

---

## 🚀 Como Executar os Exercícios

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/JhArantes/Exercicios_Teste_Hipotese
    ```

2.  **Instale as dependências:**
    ```bash
    pip install scipy pandas matplotlib
    ```

3.  **Exemplo de uso rápido (Teste T Independente):**
    ```python
    from scipy.stats import ttest_rel, ttest_ind, ttest_1samp, norm
    import pandas as pd

    # Exemplo: Nível de glicose entre dois grupos
    grupo_a = [95, 102, 98, 110, 105]
    grupo_b = [115, 120, 118, 125, 122]

    t_stat, p_value, df = ttest_ind(grupo_a, grupo_b, alternative='two-sided')
    print(f"P-valor: {p_value:.4f}")
    ```

---

## 📂 Estrutura do Repositório

* `/data`: Datasets fictícios e reais de saúde (CSV).
* `/notebooks`: Jupyter Notebooks detalhados com a explicação teórica e código.
* `/src`: Scripts Python com funções auxiliares para automação dos testes.

---

## 📝 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para usar e colaborar!