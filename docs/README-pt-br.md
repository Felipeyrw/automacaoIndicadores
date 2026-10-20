<div align="center">

# Automação de Indicadores Empresariais

**Cálculo automatizado de KPIs, validação de metas e envio de relatórios personalizados por e-mail.**

Um projeto de automação em Python desenvolvido para transformar dados de planilhas em informações sobre o desempenho de negócios.

</div>

<p align="center">
  <strong>Language / Idioma:</strong>
  <a href="./README.md">English</a> |
  <a href="./README.pt-br.md">Português</a>
</p>

---

## Visão Geral

A **Automação de Indicadores Empresariais** é um projeto desenvolvido em Python que processa dados empresariais provenientes de planilhas, calcula indicadores-chave de desempenho (KPIs), avalia os resultados em relação a metas predefinidas e envia relatórios personalizados por e-mail para diferentes empresas.

O objetivo é reduzir o trabalho manual e repetitivo envolvido na análise de planilhas, na verificação de metas e na comunicação dos resultados de desempenho.

Em vez de calcular métricas manualmente e preparar e-mails individuais, a automação processa os dados disponíveis e gera mensagens contendo os indicadores de cada empresa e o status de suas respectivas metas.

O projeto demonstra a aplicação prática de Python, manipulação de dados, métricas de negócio e automação de e-mails para otimizar um fluxo de trabalho de análise e comunicação.

## Principais Funcionalidades

- **Processamento de planilhas:** leitura e processamento de informações empresariais.
- **Cálculo automatizado de KPIs:** cálculo de indicadores de faturamento, ticket médio e diversidade de produtos.
- **Validação de metas:** avaliação dos indicadores calculados em relação aos objetivos estabelecidos.
- **Geração de e-mails personalizados:** criação de mensagens individuais com os indicadores relevantes de cada empresa.
- **Envio automatizado de e-mails:** envio das mensagens geradas por meio de um servidor SMTP.
- **Processamento em lote:** processamento dos dados de várias empresas em uma única execução.
- **Acompanhamento da execução:** visualização da quantidade de e-mails enviados.

## Indicadores-Chave de Desempenho (KPIs)

A automação trabalha com três indicadores principais.

| Indicador | Descrição |
| --- | --- |
| Faturamento | Mede o faturamento da empresa com base nos dados disponíveis na planilha e compara o resultado com a meta correspondente. |
| Ticket Médio | Mede o valor médio por venda ou transação e compara o resultado com o objetivo estabelecido. |
| Diversidade de Produtos | Avalia a variedade de produtos de acordo com as regras de cálculo implementadas no projeto. |

Cada empresa recebe um e-mail com seus próprios resultados, facilitando a compreensão do desempenho e a identificação das metas alcançadas.

As fórmulas exatas, os valores das metas e as regras de cálculo são definidos no código-fonte do projeto.

## Como Funciona

A automação segue um fluxo de processamento de dados e comunicação.

1. **Leitura dos dados:** obtenção das informações empresariais a partir da planilha.
2. **Processamento dos registros:** organização dos dados e cálculo dos KPIs necessários.
3. **Avaliação do desempenho:** comparação dos indicadores calculados com suas respectivas metas.
4. **Geração de e-mails personalizados:** preparação de uma mensagem contendo os resultados e o status das metas de cada empresa.
5. **Envio das mensagens:** entrega dos e-mails por meio de SMTP.
6. **Conferência da execução:** verificação da saída do programa para identificar a quantidade de e-mails enviados.

Esse fluxo reduz a necessidade de cálculos manuais repetitivos e da preparação individual de mensagens.

## Tecnologias Utilizadas

| Tecnologia | Finalidade |
| --- | --- |
| Python | Implementação do fluxo de automação e das regras de negócio. |
| pandas | Manipulação e processamento dos dados da planilha. |
| smtplib | Envio de e-mails por meio de um servidor SMTP. |

### Python

Python é a linguagem utilizada para implementar a automação, processar os dados, calcular os indicadores e coordenar o envio dos e-mails.

### pandas

A biblioteca pandas permite trabalhar com dados tabulares estruturados, facilitando a organização das informações empresariais e a realização dos cálculos necessários.

### smtplib

O módulo `smtplib` faz parte da biblioteca padrão do Python e permite a comunicação com servidores SMTP para o envio de e-mails.

Normalmente, não é necessário instalá-lo separadamente.

## Demonstração do Projeto

### 1. E-mail com KPIs Personalizados

O exemplo abaixo demonstra o e-mail gerado para uma empresa.

A mensagem apresenta os indicadores calculados, incluindo faturamento, ticket médio e diversidade de produtos, e informa se as respectivas metas foram atingidas.

![Exemplo de e-mail com KPIs personalizados](../email.jpg)

### 2. Envio Automatizado de E-mails

Este exemplo demonstra o processo de envio e a quantidade de mensagens enviadas durante uma execução.

Cada mensagem é personalizada com os indicadores correspondentes à empresa destinatária.

![Exemplo do resumo de envio de e-mails](../emails.jpg)

## Como Executar

Siga as instruções abaixo para preparar o ambiente Python.

### Pré-requisitos

Antes de executar o projeto, certifique-se de ter:

- Python 3 instalado.
- O código-fonte do projeto.
- A planilha utilizada como entrada.
- Acesso a uma conta de e-mail que permita o envio por SMTP.
- As configurações e credenciais necessárias para o servidor SMTP.

### 1. Clone o Repositório

```bash
git clone <url-do-repositorio>
cd <pasta-do-repositorio>
```

Substitua os valores de exemplo pela URL real do repositório e pelo nome da pasta.

### 2. Crie um Ambiente Virtual

Recomenda-se criar um ambiente virtual para manter as dependências do projeto isoladas.

```bash
python -m venv .venv
```

Ative o ambiente no Linux ou macOS:

```bash
source .venv/bin/activate
```

No Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Instale as Dependências

Instale o pandas:

```bash
python -m pip install pandas
```

Se a planilha de entrada estiver no formato Excel, também poderá ser necessário instalar um mecanismo de leitura, como `openpyxl`, dependendo de como o código acessa o arquivo.

```bash
python -m pip install openpyxl
```

O módulo `smtplib` já faz parte da biblioteca padrão do Python.

### 4. Configure o Projeto

Antes de executar a automação:

1. Verifique se a planilha de entrada está no caminho esperado pelo script.
2. Confirme se a planilha contém as colunas necessárias para o funcionamento da implementação.
3. Confira as regras de cálculo dos KPIs e os valores das metas.
4. Configure o servidor SMTP, a porta, o endereço do remetente, a autenticação e os destinatários de acordo com o provedor de e-mail e a implementação do projeto.
5. Verifique se cada empresa está associada ao endereço de e-mail correto.

A estrutura exata da planilha, o nome do script principal e o método de configuração dependem dos arquivos presentes no repositório.

Consulte o código-fonte para identificar os valores necessários antes de executar o projeto.

### 5. Execute a Automação

Execute o script principal do projeto a partir da pasta do repositório.

```bash
python <nome-do-script>.py
```

Substitua `<nome-do-script>.py` pelo nome real do arquivo responsável por iniciar a execução.

## Segurança

Credenciais de e-mail e outras informações sensíveis nunca devem ser enviadas para um repositório público.

Boas práticas incluem:

- Armazenar credenciais em variáveis de ambiente ou em um arquivo de configuração local apropriado.
- Adicionar ao `.gitignore` os arquivos locais que contenham informações sensíveis.
- Evitar senhas de e-mail diretamente no código-fonte.
- Testar a automação com uma pequena quantidade de dados e destinatários específicos antes de enviar mensagens para várias empresas.
- Conferir o mapeamento dos destinatários para evitar que informações empresariais sejam enviadas para endereços incorretos.

Se o provedor de e-mail exigir senhas de aplicativo ou configurações adicionais de SMTP, siga os requisitos de segurança correspondentes.

## Personalização

O projeto pode ser adaptado a diferentes necessidades de análise e comunicação empresarial por meio de alterações na implementação.

Algumas possibilidades incluem:

- Modificar as regras de cálculo dos KPIs.
- Atualizar os valores das metas e os critérios de desempenho.
- Adaptar a estrutura da planilha.
- Alterar o conteúdo e a formatação dos e-mails.
- Atualizar as configurações SMTP e os destinatários.

As alterações devem ser testadas com dados de exemplo para garantir que os cálculos e a avaliação das metas produzam os resultados esperados.

## Possíveis Melhorias Futuras

As seguintes melhorias poderiam ampliar o projeto em versões futuras:

- **Validação dos dados de entrada:** identificação de valores ausentes, inconsistentes ou inválidos na planilha.
- **Logs estruturados:** registro das etapas do processamento e dos erros para facilitar a investigação de problemas.
- **Tratamento de falhas de envio:** diferenciação entre e-mails enviados com sucesso e tentativas que falharam.
- **Gerenciamento de configurações:** centralização de valores configuráveis e credenciais.
- **Testes automatizados:** validação dos cálculos dos KPIs e das regras de avaliação das metas.
- **Resumo da execução:** apresentação mais detalhada dos resultados do processamento.

Esses itens são possibilidades de evolução, não funcionalidades necessariamente existentes na versão atual.

## Aprendizados do Projeto

Este projeto proporciona experiência prática com:

- Automação de tarefas utilizando Python.
- Processamento de dados com pandas.
- Cálculo e avaliação de indicadores de desempenho empresarial.
- Manipulação de dados provenientes de planilhas.
- Automação de comunicações personalizadas por e-mail utilizando SMTP.
- Transformação de necessidades de negócio em um fluxo técnico repetível.

## Licença

Nenhuma licença foi especificada para este projeto.

Caso pretenda disponibilizar o código-fonte para reutilização pública, considere adicionar um arquivo `LICENSE` apropriado.

---

<div align="center">

**Automação de Indicadores Empresariais**

Desenvolvido com Python e pandas.

</div>
