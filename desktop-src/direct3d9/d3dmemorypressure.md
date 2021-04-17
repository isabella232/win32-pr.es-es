---
description: Contiene datos de informes de presión de memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Estructura D3DMEMORYPRESSURE (D3d9types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718275"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Estructura D3DMEMORYPRESSURE (D3d9types. h)

Contiene datos de informes de presión de memoria.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes expulsados por el proceso durante la ejecución de la consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de bytes colocados en segmentos de memoria no óptimos debido a un espacio inadecuado dentro de los segmentos de memoria preferidos.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

La eficiencia general de las asignaciones de memoria que se colocaron en memoria no óptima. El valor se expresa como un porcentaje. Por ejemplo, el valor 95 indica que las asignaciones colocadas en segmentos de memoria no preferidos son un 95% eficaz. Este número no se debe considerar una medida exacta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
