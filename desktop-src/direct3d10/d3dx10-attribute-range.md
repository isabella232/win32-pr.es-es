---
description: Almacena una entrada de tabla de atributos.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE estructura (D3DX10. h)
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
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718434"
---
# <a name="d3dx10_attribute_range-structure"></a>Estructura del intervalo del \_ atributo D3DX10 \_

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



## <a name="members"></a>Miembros

<dl> <dt>

**AttribId**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de la tabla de atributos.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Superficie inicial.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de caras.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vértice inicial.

</dd> <dt>

**VertexCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de vértices.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (AttribId) al dibujar el marco.

El \_ tipo de intervalo de atributo LPD3DX \_ se define como un puntero a la estructura de intervalo de atributos de D3DX \_ \_ .


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
