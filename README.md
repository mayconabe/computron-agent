# 🤖 FiscalTron – Sistema de Auditoria Fiscal Inteligente

> Projeto desenvolvido pelo **Grupo Computron Agent** como entrega final da disciplina **I2A2 – Agentes Inteligentes** (Outubro/2025).

🎥 **Apresentação do projeto:** [YouTube - Projeto FiscalTron](https://www.youtube.com/watch?v=TRUW8QYcDvI)

---

## 📘 Sumário

- [Sobre o Projeto](#sobre-o-projeto)
- [Arquitetura do Sistema](#arquitetura-do-sistema)
- [Mini-Agentes Inteligentes](#mini-agentes-inteligentes)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Fluxo Operacional](#fluxo-operacional)
- [Equipe](#equipe)
- [Como Executar](#como-executar)
- [Conclusão](#conclusão)

---

## 💡 Sobre o Projeto

O **FiscalTron** é uma plataforma inteligente voltada à **automação da verificação fiscal**, combinando **agentes autônomos de inteligência artificial** com automações orquestradas para análise de documentos fiscais (NF-e e NFS-e).  
O sistema realiza **extração de dados via OCR**, **validações fiscais contextuais**, **checagem de consistência**, e **geração de alertas personalizados** para inconsistências tributárias.

O objetivo é **reduzir erros humanos**, **agilizar auditorias fiscais** e **garantir conformidade tributária** com as legislações do estado de São Paulo.

---

## 🧠 Arquitetura do Sistema

O projeto foi desenvolvido com base nos princípios de **modularidade e orquestração inteligente**, sendo composto por:

- **n8n** – orquestrador central de automações;  
- **Agentes de IA** (LLM Google Gemini e Mistral AI) – responsáveis por interpretar e validar informações fiscais;  
- **OCR.space + Mistral OCR** – dupla abordagem para extração textual e estrutural dos documentos;  
- **Banco de Dados Vetorial** – armazena embeddings e histórico de interações para consultas semânticas.

🧩 *Veja a arquitetura funcional completa no diagrama da página 8 do documento.*

---

## 🤝 Mini-Agentes Inteligentes

O FiscalTron atua como o **maestro de uma orquestra de mini-agentes**, responsáveis por tarefas específicas:

| Mini-Agente | Função |
|--------------|--------|
| **Extrator-Tron** | Leitura e extração automática via OCR de notas fiscais (valores, datas, CNPJ/CPF etc). |
| **Researcher-Tron** | Consulta de modelos LLM para contextualizar regras e doutrinas tributárias. |
| **Validador-Tron** | Checagem formal e legal dos dados (validação de cálculos, chaves e ISS). |
| **Alert-Tron** | Emissão de alertas e notificações ao usuário em caso de inconsistência. |
| **Data-Tron** | Organização e armazenamento vetorial de informações para buscas semânticas. |

---

## 🧰 Tecnologias Utilizadas

| Categoria | Tecnologias |
|------------|--------------|
| **Orquestração e Automações** | n8n |
| **IA e Modelos de Linguagem** | Google Gemini, Mistral AI |
| **OCR e Processamento de Texto** | OCR.space, Mistral OCR, Tesseract |
| **Banco de Dados Vetorial** | ChromaDB / FAISS |
| **Integrações** | Google Drive API, REST API, ERP externo |
| **Linguagens** | JavaScript (Node n8n), Python, Markdown JSON |
| **Ambiente** | Cloud-based com pipelines automatizados e logs estruturados |

---

## ⚙️ Fluxo Operacional

O workflow do **FiscalTron** segue um ciclo completo de automação:

1. **Monitoramento de pastas** no Google Drive (PDF/XML de NFS-e e NF-e);  
2. **Download e conversão Base64** dos arquivos;  
3. **Dupla extração OCR:**  
   - Texto bruto (OCR.space)  
   - Estrutura semântica (Mistral AI – Markdown)  
4. **Combinação e pré-processamento** dos resultados;  
5. **Análise por agentes de IA (Google Gemini)** com regras de validação cruzada;  
6. **Validação fiscal detalhada** (CNPJ, ISS, alíquotas, PIS/COFINS, valores totais);  
7. **Geração de relatórios e alertas** no chatbot FiscalTron;  
8. **Arquivamento automatizado** conforme sucesso ou falha no processamento.

---

## 👥 Equipe Computron Agent

| Integrante |
|-------------|
| André Matos |
| Maycon Abe |
| Sidney Wergles |
| Filipe Andrade |
| Thiago Souza |
| Maurício Abe |
| Luciano Scagliusi |
| Harding Leite |

---

## 🚀 Como Executar

> ⚠️ Este projeto é acadêmico e foi desenvolvido para fins de demonstração de orquestração de agentes inteligentes.

1. **Importe o workflow no n8n** (`.json` fornecido na pasta `/flows`).  
2. **Configure suas credenciais:**
   - Google Drive API (monitoramento de pastas)  
   - OCR.space API Key  
   - Mistral AI e Gemini API Keys  
3. **Execute manualmente o fluxo** (“Execute Workflow”).  
4. **Acompanhe o chatbot FiscalTron** para visualizar logs e relatórios.

---

## 🧩 Conclusão

O **FiscalTron** demonstra o potencial dos **agentes inteligentes** aplicados à automação fiscal e contábil.  
A combinação entre **IA cognitiva**, **OCR duplo**, **validação automatizada** e **chatbot interativo** permite um sistema escalável, auditável e didático — um passo rumo à **governança tributária inteligente**.

---
