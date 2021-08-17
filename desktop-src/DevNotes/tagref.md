---
description: 'TAGREF: contiene el índice de una entrada y su información de ETIQUETA en una base de datos shim.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075788"
---
# <a name="tagref"></a>TAGREF

Contiene el índice de una entrada y su información tag en una base de datos shim.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Comentarios

Un **TAGREF es específico** de una base de datos shim y es válido en varias bases de datos. Puede ser un valor entero que representa el índice o uno de los siguientes valores:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)
</dt> <dd>

**TAGREF** no existe. Este valor se devuelve de una función cuando no puede devolver un **TAGREF válido.**

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)
</dt> <dd>

Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **ELEMENTO TAGREF secundario.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**etiqueta**](tag.md)
</dt> <dt>

[Tipos DE ETIQUETA](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




