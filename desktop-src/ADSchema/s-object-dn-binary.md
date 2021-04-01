---
title: Sintaxis de Object (DN-Binary)
description: Cadena de octetos que contiene un valor binario y un nombre distintivo (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DN-binario)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151293"
---
# <a name="objectdn-binary-syntax"></a>Sintaxis de Object (DN-Binary)

Cadena de octetos que contiene un valor binario y un nombre distintivo (DN).



| Entrada | Value |
|--------------|------------------------------------------------------------------------------------|
| Nombre         | Object(DN-Binary)                                                                  |
| IDENTIFICADOR de sintaxis    | 2.5.5.7                                                                            |
| IDENTIFICADOR DE OM        | 127                                                                                |
| Tipo MAPI    | TSTRING                                                                            |
| Tipo ADS     | \_DN ADSTYPE \_ con \_ binario                                                          |
| Tipo Variant | distribución de VT \_                                                                       |
| Tipo de SDS     | Objeto COM que se puede convertir en un [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Observaciones

Un valor con esta sintaxis tiene el formato siguiente:

``` syntax
B:<char count>:<binary value>:<object DN>
```

donde " &lt; número &gt; de caracteres" es el número de dígitos hexadecimales en " &lt; valor binario" &gt; , " &lt; valor binario &gt; " es la representación hexadecimal del valor binario y " &lt; DN del objeto &gt; " es un nombre distintivo. Active Directory actualiza automáticamente el DN si el objeto al que hace referencia se mueve o se cambia de nombre. Para obtener más información y un ejemplo de código que use esta sintaxis, vea [Habilitar el enlace de renombre seguro con la propiedad otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
