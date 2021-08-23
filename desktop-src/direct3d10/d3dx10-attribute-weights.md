---
description: 'D3DX10_ATTRIBUTE_WEIGHTS estructura: especifica los atributos de peso de malla.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 1ef80db70d0562b000aa527afe17da43eee0eed5d6498e5da5b3d1ad964f5f87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282785"
---
# <a name="d3dx10_attribute_weights-structure"></a>Estructura D3DX10 \_ ATTRIBUTE \_ WEIGHTS

Especifica atributos de peso de malla.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
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

El tipo LPD3DX ATTRIBUTE WEIGHTS se define como un puntero a la estructura \_ \_ D3DX \_ ATTRIBUTE \_ WEIGHTS.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
