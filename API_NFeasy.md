# API de emissão de nota fiscal da empresa fictícia NFeasy

O sistema disponibiliza uma API REST para emissão de notas fiscais.

## Endpoint

POST /api/invoices

### Descrição

Cria uma nova nota fiscal no sistema.

Exemplo de requisição:

{
  "cliente": {
    "nome": "Empresa Exemplo Ltda",
    "cnpj": "12345678000100"
  },
  "produtos": [
    {
      "descricao": "Serviço de consultoria",
      "quantidade": 1,
      "valor_unitario": 1500
    }
  ],
  "data_emissao": "2026-03-09"
}
Exemplo de resposta
{
  "invoice_id": 98452,
  "status": "emitida",
  "data_emissao": "2026-03-09",
  "valor_total": 1500
}
Problemas comuns
Erro ao emitir nota fiscal

### Possíveis causas:

- Dados do cliente incompletos

- Produto não cadastrado

- Falha na comunicação com o serviço fiscal

### Solução

Verifique os dados informados e tente emitir novamente.

Caso o erro persista, entre em contato com o suporte técnico.

### Conclusão

Esta documentação apresenta as principais funcionalidades do sistema de emissão de notas fiscais, incluindo instruções de uso e exemplos de integração via API.

O objetivo é fornecer orientações claras para usuários e desenvolvedores que utilizam ou integram o sistema em seus processos operacionais.