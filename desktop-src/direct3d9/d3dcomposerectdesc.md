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
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060751"
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



## <a name="members"></a>Members

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

## <a name="remarks"></a>Observaciones

Esta estructura se usa en llamadas [**a ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir glifos en la superficie de origen. Se crea un búfer de vértices (consulte [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)rellenado con estas estructuras para contener las ubicaciones del glifo. Los miembros de USHORT se usan para reducir la superficie de memoria tanto como sea posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
