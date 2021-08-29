---
description: 'D3DX10_INTERSECT_INFO estructura: describe una intersección de triángulo de rayo.'
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO estructura (D3DX10.h)
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
ms.openlocfilehash: d4f660066205a626d6718bf8bd473d54d1d761f9ee499dd0c25a178d9846a0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753555"
---
# <a name="d3dx10_intersect_info-structure"></a>Estructura INFO de INTERSECT de D3DX10 \_ \_

Describe una intersección de triángulo de rayo.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice del triángulo que alcanzó el rayo.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada centrada en el triángulo en el que el rayo forma intersección.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada centrada en el triángulo en el que el rayo forma intersección.

</dd> <dt>

**Dist**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Distancia a lo largo del rayo donde se produjo la intersección.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
