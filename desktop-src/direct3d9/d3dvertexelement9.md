---
description: Define el diseño de los datos de vértices. Cada vértice puede contener uno o más tipos de datos, y cada tipo de datos lo describe un elemento de vértice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Estructura D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670243"
---
# <a name="d3dvertexelement9-structure"></a>Estructura D3DVERTEXELEMENT9

Define el diseño de los datos de vértices. Cada vértice puede contener uno o más tipos de datos, y cada tipo de datos lo describe un elemento de vértice.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Stream**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de secuencia.

</dd> <dt>

**Offset**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de los datos del vértice hasta los datos asociados con el tipo de datos determinado.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

El tipo de datos, especificado como [**D3DDECLTYPE**](./d3ddecltype.md). Uno de varios tipos predefinidos que definen el tamaño de los datos. Algunos métodos tienen un tipo implícito.

</dd> <dt>

**Método**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

El método especifica el procesamiento de del teselador, que determina cómo del teselador interpreta (o opera) los datos de vértices. Para obtener más información, vea [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Define para qué se usarán los datos; es decir, la interoperabilidad entre los diseños de datos de vértice y los sombreadores de vértices. Cada uso actúa para enlazar una declaración de vértice a un sombreador de vértices. En algunos casos, tienen una interpretación especial. Por ejemplo, un elemento que especifica \_ la posición D3DDECLUSAGE normal o D3DDECLUSAGE \_ se usa en la del teselador N-patch para configurar la teselación. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md) para obtener una lista de la semántica disponible. D3DDECLUSAGE \_ TEXCOORD se puede usar para campos definidos por el usuario (que no tienen definido un uso existente).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifica los datos de uso para permitir al usuario especificar varios tipos de uso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los datos de vértice se definen mediante una matriz de estructuras **D3DVERTEXELEMENT9** . Use [**D3DDECL \_ End**](d3ddecl-end.md) para declarar el último elemento de la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Declaración de vértices (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
