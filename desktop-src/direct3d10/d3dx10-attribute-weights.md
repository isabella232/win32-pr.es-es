---
description: Especifica los atributos de peso de la malla.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS estructura (D3DX10. h)
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
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362621"
---
# <a name="d3dx10_attribute_weights-structure"></a>Estructura de pesos del \_ atributo D3DX10 \_

Especifica los atributos de peso de la malla.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Ubicación.

</dd> <dt>

**Límite**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de la mezcla.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminación difusa.

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminación especular.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Ocho coordenadas de textura.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormalización**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En esta estructura se describe cómo una operación de simplificación considerará los datos de vértices al calcular los costos relativos entre los bordes contraídos. Por ejemplo, si el campo normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error de la acción de contraer. Sin embargo, si el campo normal es 1,0, la operación de simplificación usará el componente normal de vértice. Si el campo normal es 2,0, duplique la cantidad de errores; Si el campo normal es 4,0, cuádruple el número de errores, etc.

El \_ tipo de pesos del atributo LPD3DX \_ se define como un puntero a la \_ estructura de pesos del atributo D3DX \_ .


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
