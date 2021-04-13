---
description: Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538517"
---
# <a name="tagref"></a>TAGREF

Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Observaciones

Una **TAGREF** es específica de una base de datos de corrección de compatibilidad y es válida en varias bases de datos. Puede ser un valor entero que represente el índice, o uno de los valores siguientes:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)
</dt> <dd>

El **TAGREF** no existe. Este valor se devuelve de una función cuando no puede devolver un **TAGREF** válido.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Raíz TAGREF (0)
</dt> <dd>

Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **TAGREF** secundario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**ETIQUETA**](tag.md)
</dt> <dt>

[Tipos de etiquetas](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




