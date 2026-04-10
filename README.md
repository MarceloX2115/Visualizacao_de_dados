# 📊 Refatoração de Visualizações de Dados: Guia Prático

Este documento consolida as melhores práticas aplicadas na correção dos desafios de design visual, utilizando como base as teorias de Tufte, Gestalt e Cleveland-McGill.

---

## 🚀 Princípios Aplicados

### 1. Integridade Visual (Edward Tufte)
* **Fator de Mentira (Lie Factor):** Eliminamos distorções visuais. Gráficos de barras devem ter o eixo Y começando em zero para representar proporcionalidade real.
* **Data-Ink Ratio:** Maximizamos a informação útil. Removemos grids pesados, bordas (spines) e elementos decorativos que não transmitem dados.

### 2. Leis da Percepção (Gestalt)
* **Proximidade:** Rótulos de dados e legendas foram movidos para perto dos elementos gráficos, reduzindo o esforço de alternar o olhar entre legenda e dado.
* **Semelhança:** Cores foram padronizadas. Se a métrica é a mesma, a cor deve ser a mesma. Cores distintas agora indicam categorias ou alertas específicos.
* **Ordenação:** Dados foram organizados (ex: decrescente) para facilitar a comparação imediata e reduzir o processamento mental.

### 3. Eficácia da Codificação (Cleveland-McGill)
* **Posição > Área:** Substituímos gráficos de pizza por barras horizontais e melhoramos gráficos de bolhas, pois o olho humano julga posições e comprimentos com muito mais precisão do que ângulos ou áreas.

---

## 🛠️ Checklist de Refatoração

| De (Problema) | Para (Solução) | Princípio Chave |
| :--- | :--- | :--- |
| Eixo Y Truncado | Eixo Y iniciando em 0 | Integridade (Tufte) |
| Gráfico de Pizza | Gráfico de Barras | Eficácia (Cleveland) |
| Cores Aleatórias | Cores Funcionais/Neutras | Semelhança (Gestalt) |
| Chartjunk (Grids/Marcadores) | Design Minimalista | Data-Ink Ratio (Tufte) |
| Legendas Externas | Anotações Diretas | Proximidade (Gestalt) |

---

## 💻 Como Executar as Correções

As soluções foram implementadas em Python utilizando:
* **Matplotlib:** Para controle granular de eixos e textos.
* **Seaborn:** Para estética simplificada e plotagem estatística.
* **Pandas:** Para manipulação e ordenação prévia dos dados.

> **Conclusão:** Uma visualização eficiente não é aquela que tem mais elementos, mas sim aquela onde não há nada sobrando que possa distrair o tomador de decisão.
