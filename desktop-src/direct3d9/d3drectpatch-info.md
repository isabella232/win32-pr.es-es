---
description: Describe una revisión de orden superior rectangular.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707925"
---
# <a name="d3drectpatch_info-structure"></a>Estructura de información de D3DRECTPATCH \_

Describe una revisión de orden superior rectangular.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**StartVertexOffsetWidth**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de desplazamiento de vértice inicial, en número de vértices.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de desplazamiento de vértice inicial, en número de vértices.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de cada vértice, en número de vértices.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de cada vértice, en número de vértices.

</dd> <dt>

**STRI**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la matriz de vértices bidimensional imaginario, que ocupa el mismo espacio que el búfer de vértices. Para obtener un ejemplo, vea el diagrama siguiente.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define el tipo base para la revisión de orden superior rectangular.



| Value                 | Pedido admitido            | Ancho y alto                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ Bézier      | Lineal, cúbica y quinta | Width = Height = (DWORD) Order + 1 |
| D3DBASIS \_ BSPLINE     | Lineal, cúbica y quinta | Ancho = orden de > de altura (DWORD)  |
| D3DBASIS \_ interpolación | Cúbica                      | Ancho = orden de > de altura (DWORD)  |



 

</dd> <dt>

**Grado**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , que define el grado de la revisión rectangular.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el diagrama siguiente se identifican los parámetros que especifican una revisión de rectángulo.

![diagrama de una revisión rectangular de orden superior y los parámetros que lo especifican](images/hop-rectpatch.png)

Cada uno de los vértices del búfer de vértices se muestra como un punto negro. En este caso, el búfer de vértices tiene 20 vértices en él, 16 de los cuales se encuentran en la revisión del rectángulo. STRIDE es el número de vértices en el ancho del búfer de vértices, en este caso cinco. El desplazamiento x al primer vértice se denomina StartIndexVertexWidth y en este caso 1. El desplazamiento y al primer vértice de la revisión se denomina StartIndexVertexHeight y, en este caso, 0.

Para representar una secuencia de revisiones rectangulares individuales (sin mosaico), debe interpretar la geometría como una revisión rectangular larga (1 x N) rectangular. La estructura de **\_ información de D3DRECTPATCH** para esta franja (Bézier cúbica) se configuraría de la siguiente manera.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
