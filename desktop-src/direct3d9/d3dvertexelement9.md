---
description: Define el diseño de datos del vértice. Cada vértice puede contener uno o varios tipos de datos y cada tipo de datos se describe mediante un elemento de vértice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Estructura D3DVERTEXELEMENT9 (D3D9Types.h)
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
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527299"
---
# <a name="d3dvertexelement9-structure"></a>Estructura D3DVERTEXELEMENT9

Define el diseño de datos del vértice. Cada vértice puede contener uno o varios tipos de datos y cada tipo de datos se describe mediante un elemento de vértice.

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

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de secuencia.

</dd> <dt>

**Offset**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de los datos del vértice a los datos asociados al tipo de datos determinado.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo de datos, especificado como [**D3DDECLTYPE**](./d3ddecltype.md). Uno de varios tipos predefinidos que definen el tamaño de los datos. Algunos métodos tienen un tipo implícito.

</dd> <dt>

**Método**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

El método especifica el procesamiento del teselador, que determina cómo interpreta (o opera) el teselador los datos del vértice. Para obtener más información, [**vea D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Define para qué se usarán los datos; es decir, la interoperabilidad entre los diseños de datos de vértices y los sombreadores de vértices. Cada uso actúa para enlazar una declaración de vértice a un sombreador de vértices. En algunos casos, tienen una interpretación especial. Por ejemplo, el teselador N-patch usa un elemento que especifica D3DDECLUSAGE NORMAL o D3DDECLUSAGE POSITION para configurar la \_ \_ teselación. Consulte [**D3DDECLUSAGE para**](./d3ddeclusage.md) obtener una lista de la semántica disponible. D3DDECLUSAGE TEXCOORD se puede usar para campos definidos por el usuario (que no tienen definido un \_ uso existente).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifica los datos de uso para permitir al usuario especificar varios tipos de uso.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los datos de vértice se definen mediante una matriz de **estructuras D3DVERTEXELEMENT9.** Use [**D3DDECL \_ END para**](d3ddecl-end.md) declarar el último elemento de la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Declaración de vértice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
