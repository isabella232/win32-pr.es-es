---
title: Estructura de direntary
description: Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menús de la estructura de direntary y otros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802672"
---
# <a name="direntry-structure"></a>Estructura de direntary

Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **Word**

</dd> <dd>

Identificador ordinal único para una fuente individual de un grupo de recursos de fuente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura [**FONTDIRENTRY**](fontdirentry.md) de la fuente especificada sigue directamente a **la estructura de la misma** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





