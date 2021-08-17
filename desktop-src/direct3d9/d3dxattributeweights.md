---
description: 'Estructura D3DXATTRIBUTEWEIGHTS: especifica atributos de peso de malla.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estructura D3DXATTRIBUTEWEIGHTS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fa40476bdd1f65dddf0f78b57cfca2b20ac7bd8186eaf78546ddda9b3fa8771a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096600"
---
# <a name="d3dxattributeweights-structure"></a>D3DXATTRIBUTEWEIGHTS (estructura)

Especifica los atributos de peso de malla.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Position**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ubicación.

</dd> <dt>

**Límite**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de mezcla.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminación difusa.

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminación especular.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ocho coordenadas de textura.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En esta estructura se describe cómo una operación de simplificación considerará los datos de vértices al calcular los costos relativos entre los bordes con contraer. Por ejemplo, si el campo Normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error para el contrae. Sin embargo, si el campo Normal es 1.0, la operación de simplificación usará el componente normal del vértice. Si el campo Normal es 2.0, duplicó la cantidad de errores; si el campo Normal es 4.0, a continuación, el número de errores, y así sucesivamente.

El tipo LPD3DXATTRIBUTEWEIGHTS se define como un puntero a la **estructura D3DXATTRIBUTEWEIGHTS.**


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
