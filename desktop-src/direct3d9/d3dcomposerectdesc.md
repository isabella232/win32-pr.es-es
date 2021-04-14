---
description: Especifica el rectángulo que se usa para incluir glifos en una superficie monocroma.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Estructura D3DCOMPOSERECTDESC (D3d9types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424347"
---
# <a name="d3dcomposerectdesc-structure"></a>Estructura D3DCOMPOSERECTDESC

Especifica el rectángulo que se usa para incluir glifos en una superficie monocroma.

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

Coordenada izquierda en la que se va a comenzar la copia.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada superior en la que se va a comenzar la copia.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de textura de la coordenada izquierda.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de textura de la coordenada superior.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se utiliza en las llamadas a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir los glifos en la superficie de origen. Se crea un búfer de vértices (vea [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) rellenado con estas estructuras para que contenga las ubicaciones del glifo. Los miembros USHORT se usan para reducir la superficie de memoria tanto como sea posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
