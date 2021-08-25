---
description: Describe una revisión rectangular de orden superior.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO estructura (D3D9Types.h)
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
ms.openlocfilehash: b73ebc548031fd931cce0d34edfadf81a73d71d60edf649718875c52cfc992f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850235"
---
# <a name="d3drectpatch_info-structure"></a>Estructura INFO D3DRECTPATCH \_

Describe una revisión rectangular de orden superior.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de desplazamiento del vértice inicial, en número de vértices.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto inicial del desplazamiento del vértice, en número de vértices.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de cada vértice, en número de vértices.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de cada vértice, en número de vértices.

</dd> <dt>

**Paso**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la matriz de vértices bidimensional imaginaria, que ocupa el mismo espacio que el búfer de vértices. Para obtener un ejemplo, vea el diagrama siguiente.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Miembro del tipo [**enumerado D3DBASISTYPE,**](./d3dbasistype.md) que define el tipo base de la revisión rectangular de orden superior.



| Value                 | Pedido admitido            | Ancho y alto                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ BEZIER      | Lineal, cúbica y cúbica | Width = height = (DWORD)order + 1 |
| D3DBASIS \_ BSPLINE     | Lineal, cúbica y cúbica | Width = height > (DWORD)order  |
| INTERPOLACIÓN D3DBASIS \_ | Cúbicos                      | Width = height > (DWORD)order  |



 

</dd> <dt>

**Grado**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Miembro del tipo [**enumerado D3DDEGREETYPE,**](./d3ddegreetype.md) que define el grado de la revisión rectangular.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En el diagrama siguiente se identifican los parámetros que especifican una revisión de rectángulo.

![diagrama de una revisión rectangular de orden superior y los parámetros que la especifican](images/hop-rectpatch.png)

Cada uno de los vértices del búfer de vértices se muestra como un punto negro. En este caso, el búfer de vértices tiene 20 vértices, 16 de los cuales están en la revisión del rectángulo. El paso es el número de vértices en el ancho del búfer de vértices, en este caso cinco. El desplazamiento x al primer vértice se denomina StartIndexVertexWidth y, en este caso, es 1. El desplazamiento y al primer vértice de revisión se denomina StartIndexVertexHeight y, en este caso, es 0.

Para representar una secuencia de revisiones rectangulares individuales (sin mosaico), debe interpretar la geometría como una revisión rectangular estrecha larga (1 x N). La **estructura INFO \_ D3DRECTPATCH** para este tipo de franja (Bézier cúbica) se configuraría de la siguiente manera.


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
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
