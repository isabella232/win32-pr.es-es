---
description: 'Estructura D3DXATTRIBUTERANGE: almacena una entrada de tabla de atributos.'
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Estructura D3DXATTRIBUTERANGE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116022"
---
# <a name="d3dxattributerange-structure"></a>D3DXATTRIBUTERANGE (estructura)

Almacena una entrada de tabla de atributos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AttribId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabla de atributos.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Cara inicial.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de caras.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Vértice inicial.

</dd> <dt>

**VertexCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Recuento de vértices.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.

El tipo LPD3DXATTRIBUTERANGE se define como un puntero a la **estructura D3DXATTRIBUTERANGE.**


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
