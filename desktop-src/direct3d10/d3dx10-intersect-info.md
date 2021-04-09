---
description: Describe una intersección de triángulo.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO estructura (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821175"
---
# <a name="d3dx10_intersect_info-structure"></a>D3DX10 \_ estructura de información de intersección \_

Describe una intersección de triángulo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FaceIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice del triángulo que ha alcanzado el rayo.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.

</dd> <dt>

**Tribu**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Distancia a lo largo del rayo en el que se produjo la intersección.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
