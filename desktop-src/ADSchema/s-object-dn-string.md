---
title: Sintaxis de Object (DN-String)
description: Cadena de octetos que contiene un valor de cadena y un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Sintaxis de objeto (DN-cadena) esquema de AD
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658463"
---
# <a name="objectdn-string-syntax"></a>Sintaxis de Object (DN-String)

Cadena de octetos que contiene un valor de cadena y un DN.



| Entrada | Value |
|--------------|------------------------------------------------------------------------------------|
| Nombre         | Object(DN-String)                                                                  |
| IDENTIFICADOR de sintaxis    | 2.5.5.14                                                                           |
| IDENTIFICADOR DE OM        | 127                                                                                |
| Tipo MAPI    | \-                                                                                 |
| Tipo ADS     | \_DN ADSTYPE \_ con \_ cadena                                                          |
| Tipo Variant | distribución de VT \_                                                                       |
| Tipo de SDS     | Objeto COM que se puede convertir en un [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Observaciones

Un valor con esta sintaxis tiene el formato siguiente:

``` syntax
S:<char count>:<string value>:<object DN>
```

donde " &lt; Char Count &gt; " es el número de caracteres de la &lt; cadena "valor de cadena &gt; " y " &lt; DN del objeto &gt; " es un nombre distintivo de un objeto en Active Directory. Active Directory actualiza el DN si el objeto al que hace referencia se mueve o se cambia de nombre.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
