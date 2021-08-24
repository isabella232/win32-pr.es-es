---
title: Sintaxis de objeto (DN-String)
description: Cadena de octeto que contiene un valor de cadena y un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DN-String)
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18222343a5c10b7231d174021c8d4238ba075b66b648d99a704f4e1d1d651e2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580255"
---
# <a name="objectdn-string-syntax"></a>Sintaxis de objeto (DN-String)

Cadena de octeto que contiene un valor de cadena y un DN.



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nombre         | Object(DN-String)                                                                  |
| Identificador de sintaxis    | 2.5.5.14                                                                           |
| Id. de OM        | 127                                                                                |
| Tipo DE MAPI    | \-                                                                                 |
| ADS Type     | ADSTYPE \_ DN \_ WITH \_ STRING                                                          |
| Tipo de variante | VT \_ DISPATCH                                                                       |
| Tipo sds     | Objeto COM que se puede convertir en [**un IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Comentarios

Un valor con esta sintaxis tiene el formato siguiente:

``` syntax
S:<char count>:<string value>:<object DN>
```

donde " char count " es el número de caracteres del " valor de cadena " cadena, y " DN de objeto " es un nombre distintivo de un &lt; &gt; objeto en &lt; &gt; &lt; &gt; Active Directory. Active Directory actualiza el DN si se mueve o se cambia el nombre del objeto al que hace referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
