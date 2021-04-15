---
title: DRM_COPY_OPL estructura (wmdrmsdk. h)
description: La estructura de copia del OPL de DRM \_ \_ contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709044"
---
# <a name="drm_copy_opl-structure"></a>Estructura del OPL de \_ copia de DRM \_

La estructura de **\_ copia del \_ OPL de DRM** contiene información sobre los niveles de protección de salida (OPLs) especificados en una licencia para las acciones de copia.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

Mínimo de OPL para las acciones de copia.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ OPL la estructura de los \_ \_ identificadores de salida**](drmdrm-opl-output-ids.md) que contiene los identificadores de las tecnologías que se van a permitir. Este miembro se usa para las tecnologías de salida que tienen asignado OPLs inferior al nivel mínimo de copia, pero en el que se puede copiar el contenido.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) la estructura de IDS de salida que contiene los identificadores de salida de tecnologías que se van a restringir. Este miembro se usa para las tecnologías de salida asignadas a OPLs que superan el nivel mínimo de copia, pero que el emisor de la licencia no concede derechos de copia en.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**el \_ OPL de reproducción de DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





