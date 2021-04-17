---
description: Especifica el glifo de origen y la ubicación en una superficie monocroma en la que copiar los glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estructura D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717664"
---
# <a name="d3dcomposerectdestination-structure"></a>Estructura D3DCOMPOSERECTDESTINATION

Especifica el glifo de origen y la ubicación en una superficie monocroma en la que copiar los glifos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Glifo determinado del índice del búfer de vértices que contiene estructuras [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado para la alineación.

</dd> <dt>

**X**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada izquierda en la que se va a comenzar la copia.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada superior en la que se va a comenzar la copia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se utiliza en las llamadas a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar que los glifos de ubicación se deben copiar en y qué glifo determinado debe copiarse. Se crea un búfer de vértices (vea [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) rellenado con estas estructuras para que contenga las ubicaciones del glifo. Los miembros USHORT se usan para reducir la superficie de memoria tanto como sea posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
