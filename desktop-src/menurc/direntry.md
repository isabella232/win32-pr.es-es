---
title: Direntry (estructura)
description: Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuente. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menús de estructura DIRENTRY y otros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 281ede8b2f87e73bf0600d985abd3194a83e8e8f186fa8f780f18f80985e0f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602115"
---
# <a name="direntry-structure"></a>Direntry (estructura)

Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuente. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**fontOrdinal**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificador ordinal único para una fuente individual en un grupo de recursos de fuente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**estructura FONTDIRENTRY**](fontdirentry.md) de la fuente especificada sigue directamente a la **estructura DIRENTRY** de esa fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





