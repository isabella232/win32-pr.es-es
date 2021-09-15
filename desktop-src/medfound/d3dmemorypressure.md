---
description: Esta estructura contiene datos para los informes de presión de memoria.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Estructura D3DMEMORYPRESSURE (D3d9types.h) para Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569445"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Estructura D3DMEMORYPRESSURE (D3d9types.h) para Microsoft Media Foundation

Contiene datos para los informes de presión de memoria.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Members

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Número de bytes que el proceso expulsó durante la consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Número total de bytes colocados en segmentos de memoria no inadecuados, debido a un espacio inadecuado dentro de los segmentos de memoria preferidos.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

La eficacia general de las asignaciones de memoria que se colocaron en memoria no óptima. El valor se expresa como un porcentaje. Por ejemplo, el valor 95 indica que las asignaciones colocadas en segmentos de memoria no mencionados son un 95 % eficientes. Este número no debe considerarse una medida exacta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7 aplicaciones \[ de escritorio\]                                                              |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]                                                 |
| Encabezado                  | D3d9types.h (incluir D3d9.h) |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Informes de presión de memoria](memory-pressure-reporting.md)
</dt> </dl>

 

 




