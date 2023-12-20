---
title: "request"
---

# request

Objeto que representa uma requisição.


## Atributos

{{< details "host - <i>string</i>" close >}}

O *hostname* do request. Exemplo: `demostore.myshoppub.com`.

{{< /details >}}

---

{{< details "path - <i>string</i>" close >}}

O *path* do request. Exemplos:
- `/` (sendo a *home*)
- `/produto/dunk-low-retro-mens-shoes/` (sendo um *detalhe de produto*)

> **Nota**
> 
> Se a página em questão for *404 (não encontrada)* então o valor será `null`.

{{< /details >}}

---

{{< details "page_type - <i>string</i> de uma lista de valores" close >}}

O *tipo de página* que está sendo requisitada.

| Possíveis valores |
| ----------------- |
| `home` |
| `product` |
| `page` |
| `search` |
| `category` |

{{< /details >}}

---

{{< details "origin - <i>string</i>" close >}}

Valor pré-concatenado com o *schema* da requisição, sendo `https://{request.host}`.

{{< /details >}}

## Exemplos

### Exemplo 1
``` json
{
    "host": "demostore.myshoppub.com",
    "path": "/produto/dunk-low-retro-mens-shoes/",
    "page_type": "product",
    "origin": "https://demostore.myshoppub.com"
}
```

### Exemplo 2
``` json
{
    "host": "demostore.myshoppub.com",
    "path": null,
    "page_type": "404",
    "origin": "https://demostore.myshoppub.com"
}
```