---
title: DRM_COPY_OPL estructura (Wmdrmsdk.h)
description: La estructura OPL copy de DRM contiene información sobre los niveles de protección \_ \_ de salida (OL) especificados en una licencia para las acciones de copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: d2ec6e376b2df4cd3e5462766d6fd992ed7d2356a1bc81d0ff74c662a99697af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708985"
---
# <a name="drm_copy_opl-structure"></a>Estructura \_ OPL de COPIA DE DRM \_

La **estructura \_ \_ OPL copy de DRM** contiene información sobre los niveles de protección de salida (OL) especificados en una licencia para las acciones de copia.

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

OPL mínimo para las acciones de copia.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ Estructura OPL \_ OUTPUT \_ IDS**](drmdrm-opl-output-ids.md) que contiene los identificadores de tecnologías que se permiten. Este miembro se usa para las tecnologías de salida a las que se asignan LAS OPERACIONES inferiores al nivel mínimo de copia, pero en las que se puede copiar el contenido.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ Estructura OPL \_ OUTPUT \_ IDS**](drmdrm-opl-output-ids.md) que contiene los identificadores de salida de las tecnologías que se deben restringir. Este miembro se usa para las tecnologías de salida a las que se asignan LASO que superan el nivel mínimo de copia, pero que el emisor de la licencia no concede derechos para la copia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





