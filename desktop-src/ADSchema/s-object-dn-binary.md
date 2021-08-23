---
title: Sintaxis de objeto (DN-Binary)
description: Cadena de octeto que contiene un valor binario y un nombre distintivo (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DN-Binary)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15172a8577cf8ccec71053c3d374b389d71d3264fcc1934b19440a3f9efc4904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702575"
---
# <a name="objectdn-binary-syntax"></a>Sintaxis de objeto (DN-Binary)

Cadena de octeto que contiene un valor binario y un nombre distintivo (DN).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nombre         | Object(DN-Binary)                                                                  |
| Identificador de sintaxis    | 2.5.5.7                                                                            |
| Id. de OM        | 127                                                                                |
| Tipo DE MAPI    | TSTRING                                                                            |
| ADS Type     | ADSTYPE \_ DN \_ WITH \_ BINARY                                                          |
| Tipo de variante | VT \_ DISPATCH                                                                       |
| Tipo sds     | Objeto COM que se puede convertir en [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Comentarios

Un valor con esta sintaxis tiene el formato siguiente:

``` syntax
B:<char count>:<binary value>:<object DN>
```

donde " char count " es el número de dígitos hexadecimales en " valor binario ", " valor binario " es la representación hexadecimal del valor binario y " DN de objeto " es un nombre &lt; &gt; &lt; &gt; &lt; &gt; &lt; &gt; distintivo. Active Directory actualiza automáticamente el DN si se mueve o se cambia el nombre del objeto al que hace referencia. Para obtener más información y un ejemplo de código que usa esta sintaxis, vea [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
