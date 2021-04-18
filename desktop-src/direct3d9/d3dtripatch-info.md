---
description: Describe una revisión de orden superior triangular.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO estructura (D3D9Types. h)
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
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718398"
---
# <a name="d3dtripatch_info-structure"></a>Estructura de información de D3DTRIPATCH \_

Describe una revisión de orden superior triangular.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento de vértice inicial, en número de vértices.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de vértices.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define el tipo base para la revisión de orden superior triangular. El único valor válido para este miembro es D3DBASIS \_ Bézier.

</dd> <dt>

**Grado**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , que define el tipo de grado de la revisión de orden superior triangular.



| Value                | Número de vértices |
|----------------------|--------------------|
| D3DDEGREE \_ cúbico     | 10                 |
| \_Lineal D3DDEGREE    | 3                  |
| D3DDEGREE \_ cuadrático | N/D                |
| D3DDEGREE \_ quintal   | 21                 |



 

N/A: no disponible. No se admite.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Por ejemplo, el diagrama siguiente identifica el orden de los vértices y los números de segmento para una revisión de triángulo Bézier cúbica. El orden de los vértices determina los números de segmento usados por [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch). El desplazamiento es el número de bytes al primer vértice de la revisión del triángulo en el búfer de vértices.

![diagrama de una revisión de orden superior triangular con nueve vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
