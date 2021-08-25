---
title: show urlacl
description: Enumera las DACL de la dirección URL reservada especificada o todas las direcciones URL reservadas.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- show urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f6e2443f4cdb489f8deb6e8b61d3a808e8a0711ce13c8d71edc57001787617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900625"
---
# <a name="show-urlacl"></a>show urlacl

Enumera las DACL de la dirección URL reservada especificada o todas las direcciones URL reservadas.

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_cadena_
</dt> <dd>

Especifica la dirección URL completa. Si no se especifica, implica todas las direcciones URL.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**show urlacl url=https://+:80/MyUrl**

**show urlacl url=https://www.contoso.com:80/MyUrl**

 

 




