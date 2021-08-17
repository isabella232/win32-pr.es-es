---
description: Especifica el rectángulo usado para incluir glifos en una superficie monocromática.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Estructura D3DCOMPOSERECTDESC (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8c23868e8759b98898013ea70d8d62768f1e648eb6e5019eb52dd21ba55905b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733208"
---
# <a name="d3dcomposerectdesc-structure"></a>D3DCOMPOSERECTDESC (estructura)

Especifica el rectángulo usado para incluir glifos en una superficie monocromática.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

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

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos de textura de la coordenada izquierda.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos de textura de la coordenada superior.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en llamadas [**a ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir glifos en la superficie de origen. Se crea un búfer de vértices (consulte [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)rellenado con estas estructuras para contener las ubicaciones del glifo. Los miembros de USHORT se usan para reducir la superficie de memoria tanto como sea posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
