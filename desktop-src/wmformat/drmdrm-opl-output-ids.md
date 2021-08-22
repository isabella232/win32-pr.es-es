---
title: DRM_OPL_OUTPUT_IDS estructura (Wmdrmsdk.h)
description: La estructura OPL OUTPUT IDS de DRM contiene una serie de identificadores de salida de nivel de protección \_ \_ de salida \_ (OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265e1015dd31281043d388debc802b390e7dd2d534f426ecbe24402efffd13df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658865"
---
# <a name="drm_opl_output_ids-structure"></a>Estructura \_ DE IDENTIFICADORES DE SALIDA de OPL \_ de DRM \_

La **estructura \_ OPL OUTPUT \_ \_ IDS de DRM** contiene una serie de identificadores de salida de nivel de protección de salida (OPL).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cIds**
</dt> <dd>

Número de identificadores de la matriz a la que hace referencia **rgIds.**

</dd> <dt>

**rgIds**
</dt> <dd>

Dirección de una matriz de GUID. Cada miembro de la matriz contiene un identificador de salida de OPL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa como miembro de las estructuras [**\_ \_ OPL**](drmdrm-copy-opl.md) de DRM COPY y [**DRM PLAY \_ \_ OPL**](drmdrm-play-opl.md) para identificar grupos de identificadores de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





