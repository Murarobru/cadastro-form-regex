# Ficha de Cadastro — HTML Forms + Regex

Atividade prática da aula **"HTML: Na prática Forms"** e **"HTML: Forms com Regex"**.

## O que é

Um formulário de cadastro (`index.html`) construído em HTML puro, organizado com
`<fieldset>` e `<legend>`, contendo os seguintes campos:

- Nome Completo
- Matrícula
- Data de Nascimento (DD/MM/AAAA)
- Tipo Sanguíneo
- CPF
- RG
- CNPJ
- Inscrição Estadual
- E-mail comum
- E-mail institucional (FMP)
- Telefone
- CEP
- Endereço
- Número do Cartão
- Validade (MM/AA)
- CVV
- Lote de Venda de Peixes (código fictício)
- Latitude / Longitude
- Código de Barras (EAN-13)
- Placa de carro (padrão Mercosul)

Todos os campos possuem `<label>` associado por `id`, campos obrigatórios usam o
atributo `required`, e a maioria dos campos de texto usa o atributo `pattern`
com uma expressão regular (Regex) para validação no próprio navegador.

## Regex utilizadas

| Campo | Padrão |
|---|---|
| Nome completo | `^[A-Za-zÀ-ÖØ-öø-ÿ]+(\s[A-Za-zÀ-ÖØ-öø-ÿ]+)+$` |
| Matrícula | `^\d{6,10}$` |
| Data de nascimento | `^(0[1-9]|[12][0-9]|3[01])\/(0[1-9]|1[0-2])\/\d{4}$` |
| CPF | `^\d{3}\.\d{3}\.\d{3}-\d{2}$` |
| RG | `^\d{1,2}\.\d{3}\.\d{3}-[0-9Xx]$` |
| CNPJ | `^\d{2}\.\d{3}\.\d{3}\/\d{4}-\d{2}$` |
| Inscrição estadual | `^\d{9,12}$` |
| E-mail comum | `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$` |
| E-mail FMP | `^[a-zA-Z0-9._%+-]+@fmp\.edu\.br$` |
| Telefone | `^\(?\d{2}\)?\s?\d{4,5}-?\d{4}$` |
| CEP | `^\d{5}-\d{3}$` |
| Número do cartão | `^\d{4}[\s-]?\d{4}[\s-]?\d{4}[\s-]?\d{4}$` |
| Validade do cartão | `^(0[1-9]|1[0-2])\/\d{2}$` |
| CVV | `^\d{3,4}$` |
| Lote de venda de peixes | `^PX-\d{4}-[A-Z]{2}$` |
| Latitude/Longitude | `^-?\d{1,3}\.\d+,\s?-?\d{1,3}\.\d+$` |
| Código de barras (EAN-13) | `^\d{13}$` |
| Placa Mercosul | `^[A-Z]{3}\d[A-Z]\d{2}$` |

## Como testar

1. Abra `index.html` em qualquer navegador (não precisa de servidor).
2. Preencha os campos com dados **inválidos** para ver a borda vermelha e o
   navegador bloqueando o envio.
3. Preencha com dados **válidos** (exemplos de placeholder em cada campo) e
   clique em **Enviar Cadastro** para ver a mensagem de sucesso.

## Estrutura do repositório

```
.
├── index.html   # formulário completo
└── README.md    # este arquivo
```
