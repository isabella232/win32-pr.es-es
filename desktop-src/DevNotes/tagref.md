---
description: 'TAGREF: contiene el índice de una entrada y su información DE ETIQUETA en una base de datos de correcciones de compatibilidad (shim).'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096633"
---
# <a name="tagref"></a>TAGREF

Contiene el índice de una entrada y su información tag en una base de datos de correcciones de compatibilidad (shim).


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Comentarios

Un **TAGREF es específico** de una base de datos shim y es válido en varias bases de datos. Puede ser un valor entero que representa el índice o uno de los valores siguientes:

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**etiqueta**](tag.md)
</dt> <dt>

[Tipos TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




