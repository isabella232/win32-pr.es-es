---
description: Especifica el glifo de origen y la ubicación en una superficie monocromática en la que se copian los glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estructura D3DCOMPOSERECTDESTINATION (D3d9types.h)
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
ms.openlocfilehash: e6d859cb0bfd47c9be21f37feef287b38cdce4cc64360dd312b2b52bb825a23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123315"
---
# <a name="d3dcomposerectdestination-structure"></a>D3DCOMPOSERECTDESTINATION (estructura)

Especifica el glifo de origen y la ubicación en una superficie monocromática en la que se copian los glifos.

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

Indexar un glifo determinado del búfer de vértice que contiene estructuras [**D3DCOMPOSERECTDESC.**](d3dcomposerectdesc.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado para fines de alineación.

</dd> <dt>

**X**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada izquierda en la que empezar a copiar.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada superior en la que empezar a copiar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en llamadas a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar los glifos de ubicación en los que se deben copiar y qué glifo concreto se debe copiar. Se crea un búfer de vértices (consulte [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)rellenado con estas estructuras para contener las ubicaciones del glifo. Los miembros de USHORT se usan para reducir la superficie de memoria tanto como sea posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
