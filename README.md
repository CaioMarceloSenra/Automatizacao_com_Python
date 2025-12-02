# Automatizacao_com_Python
Automação RPA com Python (PyAutoGUI + Pandas) para integração de dados entre Excel e sistemas Desktop legados.

# 🤖 Automação de Cadastro (RPA com Python)

Este projeto é uma solução de **RPA (Robotic Process Automation)** desenvolvida para automatizar o processo de cadastro de alunos em um sistema de gestão educacional (ERP Desktop).

O script substitui a digitação manual, lendo dados tratados diretamente de uma planilha Excel e interagindo com a interface gráfica do sistema legado.

## 🚀 O Problema Resolvido
O processo anterior exigia que um analista lesse um PDF/Excel e digitasse manualmente os dados de centenas de alunos, um por um. Isso gerava:
* Alto tempo de operação (8 min/aluno manualmente vs automação em background).
* Risco de erros de digitação (Typos).
* Fadiga em tarefas repetitivas.

## 🛠️ Tecnologias Utilizadas
* **Python 3.x**
* **Pandas:** Para leitura, limpeza e estruturação dos dados (ETL).
* **PyAutoGUI:** Para controle de mouse, teclado e reconhecimento de interface.
* **OpenPyXL:** Engine para manipulação de arquivos .xlsx.

## ✨ Funcionalidades Principais
* **Leitura Inteligente:** O robô identifica colunas específicas (Nome, Email, Celular) independente da ordem no Excel.
* **Sanitização de Dados:** Função automática que limpa formatações de telefone `(XX) 9XXXX-XXXX` para apenas números, evitando erros no sistema.
* **Gestão de Latência:** Pausas estratégicas entre cliques para respeitar o tempo de carregamento do sistema.
* **Pop-up Killer:** Função assíncrona que vigia e fecha pop-ups de atualização do sistema que poderiam interromper o fluxo.

## ⚙️ Como Funciona a Lógica
1.  O script carrega o arquivo `dados_alunos.xlsx`.
2.  Realiza a limpeza dos dados (remove vazios e caracteres especiais).
3.  Inicia um loop de iteração sobre cada aluno.
4.  O `PyAutoGUI` assume o controle, navegando pelos menus, preenchendo campos e salvando o registro.
5.  O sistema aguarda o tempo de processamento do banco de dados antes de reiniciar o ciclo.

## ⚠️ Disclaimer
Este repositório contém apenas o código-fonte da automação. Dados sensíveis de alunos foram anonimizados ou removidos para conformidade com a LGPD. O sistema alvo é proprietário e não está incluído.

---
**Autor:** Caio Marcelo Nepomuceno Senra
(https://www.linkedin.com/in/caio-marcelo-57aba4381/)

