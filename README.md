# 🦷 SiGOS - Sistema de Gestão de Odontologia Social

Parceria comunitária de impacto social e tecnológico desenvolvida para a clínica Click Dent em cooperação com as Atividades Curriculares de Extensão (ACE) e o Projeto Integrador I (PI-I) do UniCEUB.


# 🚀 Links Rápidos do Projeto

- 🌐 **Acesso ao Portal Online:** [SiGOS Pages]([https://camilexaviermedina.github.io/sigos-repository/src/SiGOS.Web/index.html](https://camilexaviermedina.github.io/sigos-repository/))
- 🎨 **Protótipo Interativo UI/UX:** Figma SiGOS Design
- 📅 **Quadro Scrumban de Atividades:** Trello de Gerenciamento


# 📝 Visão Geral

O **SiGOS** é uma plataforma Web responsiva projetada sob a arquitetura MVC com o objetivo de digitalizar e automatizar o controle de vagas filantrópicas odontológicas voltadas a estudantes universitários de baixa renda no Distrito Federal.

O sistema atua como uma barreira lógica de proteção operacional e financeira para a clínica parceira Click Dent, extinguindo processos manuais de triagem e planilhas analógicas e substituindo-os por uma governança digital ética, segura e em total conformidade com as diretrizes da LGPD.


# ⚙️ Regras de Negócio e Funcionalidades Críticas

## 🔒 Trava de Segurança de Cota Mensal (RF03)

O sistema monitora as confirmações e bloqueia automaticamente novos agendamentos sociais assim que o limite rígido de **3 (três) vagas confirmadas por mês** é atingido.

**Aₘₐₓ ≤ 3**

Novas solicitações são automaticamente direcionadas para uma lista de espera passiva.



## 🚫 Suspensão e Controle de No-Show (RF04 / RN05)

Caso o estudante falte sem justificativa prévia de 24 horas, o cirurgião-dentista pode registrar um evento de **No-Show**.

O sistema:

- Bloqueia automaticamente o CPF do estudante;
- Impede novos agendamentos;
- Mantém a suspensão por **180 dias (6 meses)**.



## 📊 Algoritmo de Priorização Social (RF06)

A fila de triagem é organizada automaticamente por um algoritmo de prioridade social:

- 3 candidatos da **Faixa A** (menor renda);
- Para cada 1 candidato da **Faixa B**.

Representação lógica:

**3 × 1 (Faixa A : Faixa B)**



## ⏱️ Alerta de Monitoramento de Cadeira (RF05)

Ao iniciar o atendimento odontológico, um cronômetro clínico é disparado.

Caso o procedimento ultrapasse:

**1h15min (75 minutos)**

uma notificação visual é exibida na secretaria para evitar impactos na agenda comercial da clínica.



## 🔐 Criptografia de Renda RSA-2048 (RN08 / RNF03)

Para proteção dos dados socioeconômicos sensíveis e conformidade com a LGPD:

- Arquivos de comprovante de renda são protegidos por criptografia RSA-2048;
- Dados são protegidos em trânsito;
- Dados permanecem protegidos em repouso no servidor.



# 📂 Estrutura de Arquivos e Organização do Repositório

```text
projeto-integrador-sigos/
│
├── .gitignore
├── README.md
├── index.html
├── dashboard_secretaria.html
│
├── docs/
│   ├── PI_SiGOS_Final_Consolidado.md
│   ├── ACE_Relatorio_Final_SiGOS.md
│   ├── documento_arquitetura_sigos.md
│   └── sigos_requisitos_srs.md
│
├── src/
│   ├── SiGOS.Web/
│   │   └── index.html
│   │
│   └── SiGOS.Console/
│       └── Program.cs
```



# 🛠️ Stack Tecnológica

## Frontend

- HTML5
- CSS3
- Tailwind CSS
- Font Awesome

## Backend

- C# (.NET 8)
- Entity Framework Core

## Banco de Dados

- PostgreSQL 14+ (Produção)
- SQLite (Desenvolvimento)

## Modelagem e Documentação

- brModelo
- dbdiagram.io
- Lucidchart

## Versionamento

- Git
- GitHub
- GitHub Pages



# 💻 Como Rodar o Projeto Localmente

## 1. Executando o Frontend

Como a interface foi consolidada em uma aplicação estática compatível com GitHub Pages, basta abrir o arquivo:

```text
index.html
```

### Via Windows Explorer

Clique duas vezes no arquivo:

```text
index.html
```

### Via Terminal (PowerShell ou VS Code)

```powershell
start .\index.html
```


## 2. Executando o Motor de Regras (Backend C#)

Acesse a pasta do projeto:

```powershell
cd src/SiGOS.Console
```

Execute:

```powershell
dotnet run
```



# 👥 Responsáveis pelo Projeto

## 👩‍💻 Desenvolvedora e Product Owner

**Camile Xavier Medina**  
Estudante de Análise e Desenvolvimento de Sistemas – UniCEUB



## 🏥 Patrocinador e Stakeholder

**Daniel da Cunha Pereira Luz**  
Click Dent / Inova Simples



## 🎓 Professor Orientador

**Prof. Valdemir S. Silva**  
Centro Universitário de Brasília – UniCEUB



# 📄 Licença

Projeto desenvolvido exclusivamente para fins acadêmicos, extensionistas e de impacto social no âmbito do Projeto Integrador I (PI-I) e das Atividades Curriculares de Extensão (ACE) do UniCEUB.
