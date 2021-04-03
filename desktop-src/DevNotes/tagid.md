---
description: Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998177"
---
# <a name="tagid"></a>TAGID

Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Observaciones

Un **TAGID** es específico de una base de datos. Puede ser un valor entero que represente el índice, o uno de los valores siguientes:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)
</dt> <dd>

El **TAGID** no existe. Este valor se devuelve de una función cuando no puede devolver un valor de **TAGID** válido.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>Carpeta de TAGID \_ (0)
</dt> <dd>

Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **TAGID** secundario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ETIQUETA**](tag.md)
</dt> <dt>

[Tipos de etiquetas](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




