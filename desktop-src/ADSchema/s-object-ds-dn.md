---
title: Sintaxis de objeto (DS-DN)
description: Cadena que contiene un nombre distintivo (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835688"
---
# <a name="objectds-dn-syntax"></a>Sintaxis de objeto (DS-DN)

Cadena que contiene un nombre distintivo (DN). Para los atributos con esta sintaxis, Active Directory los valores de atributo como referencias al objeto identificado por el DN y actualiza automáticamente el valor si se mueve o se cambia el nombre del objeto. Para las consultas que incluyen atributos de sintaxis DN en un filtro, especifique nombres completos distintivos. No se admiten caracteres comodín (por ejemplo, \* cn=John).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------|
| Nombre         | Object(DS-DN)                                                           |
| Identificador de sintaxis    | 2.5.5.1                                                                |
| Id. de OM        | 127                                                                    |
| Tipo DE MAPI    | OBJECT                                                                 |
| ADS Type     | ADSTYPE \_ DN \_ STRING                                                    |
| Tipo de variante | VT \_ BSTR                                                               |
| Tipo sds     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
