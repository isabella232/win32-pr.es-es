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
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360596"
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



## <a name="members"></a>Members

<dl> <dt>

**cIds**
</dt> <dd>

Número de identificadores de la matriz a la que hace referencia **rgIds.**

</dd> <dt>

**rgIds**
</dt> <dd>

Dirección de una matriz de GUID. Cada miembro de la matriz contiene un identificador de salida de OPL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como miembro de las estructuras [**\_ \_ OPL**](drmdrm-copy-opl.md) de DRM COPY y [**DRM PLAY \_ \_ OPL**](drmdrm-play-opl.md) para identificar grupos de identificadores de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





