---
title: DRM_OPL_OUTPUT_IDS estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de los ID. de salida del OPL de DRM contiene varios identificadores de salida de nivel de protección de salida (OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709012"
---
# <a name="drm_opl_output_ids-structure"></a>Estructura de IDS. de \_ salida de DRM \_ \_

La estructura de los ID. de salida del OPL de DRM contiene varios identificadores de salida de nivel de protección de salida (OPL). **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Cid**
</dt> <dd>

Número de identificadores de la matriz a los que hace referencia **rgIds**.

</dd> <dt>

**rgIds**
</dt> <dd>

Dirección de una matriz de GUID. Cada miembro de la matriz contiene un identificador de salida de OPL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como un miembro de las estructuras de la copia de DRM de la copia de los OPL y del OPL de la [**reproducción de DRM \_ \_**](drmdrm-play-opl.md) para identificar grupos de identificadores de salida. [**\_ \_**](drmdrm-copy-opl.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





