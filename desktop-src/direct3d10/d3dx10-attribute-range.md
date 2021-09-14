---
description: 'D3DX10_ATTRIBUTE_RANGE estructura: almacena una entrada de tabla de atributos.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963947"
---
# <a name="d3dx10_attribute_range-structure"></a>Estructura D3DX10 \_ ATTRIBUTE \_ RANGE

Almacena una entrada de tabla de atributos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**AttribId**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabla de atributos.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Cara inicial.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de caras.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Vértice inicial.

</dd> <dt>

**VertexCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de vértices.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.

El tipo LPD3DX ATTRIBUTE RANGE se define como un \_ puntero a la estructura \_ D3DX \_ ATTRIBUTE \_ RANGE.


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
