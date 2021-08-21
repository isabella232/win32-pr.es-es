---
description: Contiene el índice de una entrada y su información tag en una base de datos shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075789"
---
# <a name="tagid"></a>TAGID

Contiene el índice de una entrada y su información tag en una base de datos shim.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Comentarios

Un **TAGID es** específico de una base de datos. Puede ser un valor entero que representa el índice o uno de los siguientes valores:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ NULL (0)
</dt> <dd>

**TagID** no existe. Este valor se devuelve de una función cuando no puede devolver un **TAGID válido.**

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID \_ ROOT (0)
</dt> <dd>

Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **TAGID secundario.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**etiqueta**](tag.md)
</dt> <dt>

[Tipos DE ETIQUETA](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




