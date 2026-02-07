# 📊 DATASUS - SIASUS (SIA/BPA)

[![Sync Status](https://github.com/RenatoKR/SIASUS/actions/workflows/sync-datasus.yml/badge.svg)](https://github.com/RenatoKR/SIASUS/actions/workflows/sync-datasus.yml)
[![Última Atualização](https://img.shields.io/badge/última%20atualização-2026--02--07-blue)](https://github.com/RenatoKR/SIASUS/commits/main)

Repositório automatizado com mirror dos arquivos do **Sistema de Informações Ambulatoriais do SUS (SIA)** do DATASUS, incluindo:
- **BPA** - Boletim de Produção Ambulatorial
- **BDSIA** - Base de Dados SIA (Tabelas Nacionais)

## 📦 Arquivos BPA (Últimos 6 Meses)

> **Total:** 2 arquivos | **Tamanho:** 15M

| Arquivo | Competência | Tamanho | Download |
|---------|-------------|---------|----------|
| `BPAMAG0411.exe` | Novembro/2004 | 7.3M | [⬇️ Download](https://github.com/RenatoKR/SIASUS/raw/main/bpa/BPAMAG0411.exe) |
| `BPAMAG0410.exe` | Outubro/2004 | 7.3M | [⬇️ Download](https://github.com/RenatoKR/SIASUS/raw/main/bpa/BPAMAG0410.exe) |

## 🗃️ Arquivos BDSIA (Últimos 6 Meses)

> **Total:** 0 arquivos | **Tamanho:** 4.0K

| Arquivo | Competência | Tamanho | Download |
|---------|-------------|---------|----------|

## 📖 Sobre os Arquivos

### BPA - Boletim de Produção Ambulatorial
- Programa para processamento da produção ambulatorial
- Registra procedimentos realizados em estabelecimentos de saúde
- Formato: arquivo executável auto-extraível (.exe)
- Gera base de dados DBase após instalação

### BDSIA - Base de Dados SIA
- Contém as **tabelas nacionais** do Sistema de Informações Ambulatoriais
- Inclui: procedimentos, CBO, CID-10, ocupações, financiamento
- Atualizada mensalmente com novas portarias e alterações
- Essencial para validação e processamento do BPA

## 🔄 Atualização Automática

Este repositório é atualizado **diariamente às 6h (horário de Brasília)** via GitHub Actions.

**Fontes oficiais:**
- BPA: [ftp://ftp.datasus.gov.br/siasus/BPA](ftp://ftp.datasus.gov.br/siasus/BPA)
- BDSIA: [ftp://ftp.datasus.gov.br/siasus/bdsia](ftp://ftp.datasus.gov.br/siasus/bdsia)

## 💻 Como Usar

### Download via wget/curl
```bash
# Última versão do BPA
wget https://github.com/RenatoKR/SIASUS/raw/main/bpa/BPAMAG2601.exe

# Última versão do BDSIA
wget https://github.com/RenatoKR/SIASUS/raw/main/bdsia/BDSIA202601a.exe
```

### Clone do repositório
```bash
git clone https://github.com/RenatoKR/SIASUS.git
cd SIASUS
```

### GitHub API (programático)
```bash
# Listar todos os arquivos BPA
curl -s https://api.github.com/repos/RenatoKR/SIASUS/contents/bpa | jq -r '.[].download_url'

# Listar todos os arquivos BDSIA
curl -s https://api.github.com/repos/RenatoKR/SIASUS/contents/bdsia | jq -r '.[].download_url'
```

### Instalação no Windows
```cmd
# Execute os arquivos .exe para instalar
BPAMAG2601.exe
BDSIA202601a.exe
```

## 📊 Estrutura dos Arquivos

```
SIASUS/
├── bpa/                        # BPA Magnético (6 mais recentes)
│   ├── BPAMAG*.exe
│   └── BPA_LEIAME.txt
└── bdsia/                      # Base de Dados SIA (6 mais recentes)
    ├── BDSIA*.exe
    ├── BDNOTAS.TXT
    └── LERNOTAS.TXT
```

## 📝 Formato dos Arquivos

### Nomenclatura BPA
- **BPAMAG**AAMM**.exe** (ex: BPAMAG2601.exe)
  - AA = Ano (26 = 2026)
  - MM = Mês (01 = Janeiro)

### Nomenclatura BDSIA
- **BDSIA**AAAAMM**x.exe** (ex: BDSIA202601a.exe)
  - AAAA = Ano completo (2026)
  - MM = Mês (01 = Janeiro)
  - x = Revisão (a, b, c, d...)

## 🔗 Repositórios Relacionados

- [SIGTAP](https://github.com/RenatoKR/SIGTAP) - Tabela Unificada de Procedimentos

## ⚖️ Licença e Dados Públicos

Os dados são de **domínio público** e mantidos pelo Ministério da Saúde do Brasil.
Este repositório apenas facilita o acesso aos arquivos oficiais.

---

<div align="center">

**🤖 Atualizado automaticamente** | Última execução: $(date -u '+%Y-%m-%d %H:%M:%S UTC')

📦 Tamanho total: $TOTAL_SIZE

</div>
