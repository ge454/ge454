<div align="center">

# ge454

### Cibersegurança na prática · Python · Blue Team

**Dos logs de autenticação às portas de rede: construindo ferramentas para entender o que acontece em um sistema.**

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&amp;logo=python&amp;logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Blue_Team-0F172A?style=for-the-badge" alt="Blue Team" />
  <img src="https://img.shields.io/badge/An%C3%A1lise_de_logs-0891B2?style=for-the-badge" alt="Análise de logs" />
  <img src="https://img.shields.io/badge/Redes_TCP-334155?style=for-the-badge" alt="Redes TCP" />
</p>

[🛡️ Mini SOC Analyzer](https://github.com/ge454/mini-soc-analyzer) &nbsp; · &nbsp; [🌐 Port Scanner](https://github.com/ge454/port-scanner-python)

</div>

---

## Projetos em destaque

### 🛡️ Mini SOC Analyzer

**Um login aceito depois de várias falhas merece atenção.**

Ferramenta de linha de comando que analisa logs de autenticação SSH, identifica possíveis tentativas de força bruta e destaca acessos bem-sucedidos após uma sequência de falhas do mesmo IP.

- **Detecção por IP:** contagem de falhas com limite configurável.
- **Contexto para investigar:** usuários testados e horários da primeira e da última falha.
- **Priorização:** classificação de severidade em média, alta e crítica.
- **Resultado para consulta:** relatório no terminal e exportação em texto.

`Python` · `Regex` · `argparse` · `Logs SSH / syslog` · `Correlação de eventos`

**[Explorar o projeto →](https://github.com/ge454/mini-soc-analyzer#readme)** &nbsp; [Ver o código](https://github.com/ge454/mini-soc-analyzer/blob/HEAD/soc_analyzer.py)

<details>
<summary><strong>Ver um exemplo de alerta</strong></summary>

Exemplo ilustrativo com dados fictícios:

```text
[CRITICA] 203.0.113.45
    tentativas: 14 | de Nov 01 08:45:00 ate Nov 01 08:46:57
    usuarios testados: admin, oracle, root, test, ubuntu

--- ALERTA: login bem-sucedido apos varias falhas ---
203.0.113.45 entrou como 'admin' as Nov 01 08:47:10 depois de 14 falhas. Investigar.
```

</details>

---

### 🌐 SENAI Port Scanner

**Da varredura TCP ao relatório em PDF, em uma interface gráfica.**

Aplicação que verifica um intervalo de portas TCP, apresenta as portas abertas, associa serviços conhecidos pelo número da porta e tenta capturar banners de resposta.

- **Interface com Tkinter:** configuração do alvo, intervalo de portas e acompanhamento dos resultados.
- **Varredura simultânea:** execução com `ThreadPoolExecutor`.
- **Informações de rede:** portas abertas, serviços associados e banners disponíveis.
- **Relatório em PDF:** resumo da execução e tabela dos resultados quando há portas abertas.

`Python` · `socket` · `Tkinter` · `concurrent.futures` · `FPDF`

**[Explorar o projeto →](https://github.com/ge454/port-scanner-python#readme)** &nbsp; [Ver o código](https://github.com/ge454/port-scanner-python/blob/HEAD/port_scanner.py)

---

## O que estou colocando em prática

| Área | Aplicação nos projetos |
| :--- | :--- |
| **Segurança defensiva** | Identificação de padrões suspeitos e priorização de eventos de autenticação. |
| **Redes** | Conexões TCP, enumeração de portas e leitura de respostas de serviços. |
| **Desenvolvimento em Python** | Expressões regulares, linha de comando, interfaces gráficas e concorrência. |
| **Documentação de resultados** | Relatórios em texto e PDF para facilitar a análise. |

Estudo cibersegurança e uso este espaço para transformar aprendizado em ferramentas, documentar decisões e compartilhar minha evolução. Os projetos apresentados fazem parte desse percurso de estudo.

<div align="center">

**Explore o código, veja como funciona e acompanhe a evolução.**

[Todos os repositórios](https://github.com/ge454?tab=repositories)

</div>
