---
description: Describe una revisión triangular de orden superior.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850124"
---
# <a name="d3dtripatch_info-structure"></a>Estructura INFO de D3DTRIPATCH \_

Describe una revisión triangular de orden superior.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**StartVertexOffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento inicial del vértice, en número de vértices.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de vértices.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Miembro del [**tipo enumerado D3DBASISTYPE,**](./d3dbasistype.md) que define el tipo base de la revisión de orden superior triangular. El único valor válido para este miembro es D3DBASIS \_ BEZIER.

</dd> <dt>

**Grado**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Miembro del [**tipo enumerado D3DDEGREETYPE,**](./d3ddegreetype.md) que define el tipo de grado para la revisión triangular de orden superior.



| Value                | Número de vértices |
|----------------------|--------------------|
| D3DDEGREE \_ CUBIC     | 10                 |
| D3DDEGREE \_ LINEAR    | 3                  |
| D3DDEGREE \_ QUADRATIC | N/D                |
| D3DDEGREE \_ CINCOTIC   | 21                 |



 

N/A: no disponible. No compatible.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Por ejemplo, el diagrama siguiente identifica el orden de los vértices y los números de segmento de una revisión cúbica del triángulo bézier. El orden de los vértices determina los números de segmento utilizados por [**DrawTriPatch.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) El desplazamiento es el número de bytes del primer vértice de revisión de triángulo en el búfer de vértices.

![diagrama de una revisión triangular de orden superior con nueve vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
