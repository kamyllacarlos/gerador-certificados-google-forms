# Gerador Automático de Certificados Individuais

Automação para geração e envio de certificados personalizados utilizando Google Forms, Google Sheets, Google Slides, Google Drive e Google Apps Script.

O projeto permite que o participante acesse um formulário, informe seus dados e receba automaticamente seu certificado personalizado em formato PDF por e-mail.

# Sobre o projeto

A emissão manual de certificados pode envolver várias tarefas repetitivas:

* conferir os dados dos participantes;
* editar o nome no certificado;
* gerar o arquivo em PDF;
* localizar o e-mail;
* enviar o documento individualmente.

Este projeto automatiza todo esse processo.

O participante apenas preenche o formulário. O restante é realizado automaticamente pelo Google Apps Script.

# Fluxo da automação

```text
👤 Participante
       │
       ▼
📝 Google Forms
       │
       ▼
📊 Google Sheets
       │
       ▼
⚙️ Google Apps Script
       │
       ▼
🎨 Google Slides
       │
       ▼
📄 Certificado em PDF
       │
       ▼
📧 E-mail do participante
```

# Funcionalidades

* Formulário para cadastro do participante
* Captura automática do nome
* Captura automática do e-mail
* Personalização do certificado
* Geração automática de PDF
* Envio automático por e-mail
* Integração com Google Drive
* Registro das respostas no Google Sheets
* Execução automática através de gatilho do Apps Script
* Função de teste para validação do sistema

# Tecnologias utilizadas

* JavaScript
* Google Apps Script
* Google Forms
* Google Sheets
* Google Slides
* Google Drive
* MailApp

# Modelo do certificado

O certificado é criado previamente no Google Slides.

No local onde o nome deverá aparecer, é utilizado o marcador:

```text
{{NOME}}
```

Durante a execução, o sistema substitui automaticamente o marcador pelo nome informado pelo participante.

# Funcionamento

Quando o participante envia o formulário, o Apps Script recebe os dados através de um gatilho de envio.

O script:

1. identifica o nome do participante;
2. identifica o endereço de e-mail;
3. cria uma cópia do certificado modelo;
4. substitui `{{NOME}}` pelo nome informado;
5. salva a alteração;
6. converte o certificado para PDF;
7. envia o PDF para o e-mail informado.

# Testes

Antes de disponibilizar o formulário aos participantes, é recomendado realizar um teste com um endereço de e-mail próprio.

O teste permite verificar:

* leitura dos dados;
* substituição do nome;
* geração do PDF;
* envio do e-mail;
* aparência final do certificado.

# Possíveis melhorias

* Inclusão automática da data;
* Número de certificado;
* QR Code para validação;
* Página pública de autenticação;
* Personalização de outros campos;
* Diferentes modelos de certificados;
* Dashboard de certificados emitidos;
* Sistema de validação por código.

# Objetivo

O projeto foi desenvolvido para demonstrar a aplicação de **JavaScript e automação de processos** na integração de ferramentas do Google Workspace.

A solução transforma um processo manual e repetitivo em um fluxo automatizado de emissão e distribuição de documentos.

# Autora

Kamylla Carlos

Projeto desenvolvido como parte do portfólio de programação, automação e tecnologia.
