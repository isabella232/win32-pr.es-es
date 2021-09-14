---
description: Contiene datos para los informes de presión de memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Estructura D3DMEMORYPRESSURE (D3d9types.h)
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
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970987"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Estructura D3DMEMORYPRESSURE (D3d9types.h)

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

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes que el proceso expulsó durante la consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de bytes colocados en segmentos de memoria no inadecuados, debido a un espacio inadecuado dentro de los segmentos de memoria preferidos.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

La eficacia general de las asignaciones de memoria que se colocaron en memoria no óptima. El valor se expresa como un porcentaje. Por ejemplo, el valor 95 indica que las asignaciones colocadas en segmentos de memoria no mencionados son un 95 % eficientes. Este número no debe considerarse una medida exacta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
