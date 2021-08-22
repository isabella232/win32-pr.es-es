---
description: Describe una superficie de representación.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC estructura (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 838fc7d08eff0889049e7f0c73ae779239934e49049948b926fa956eeac3d40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607635"
---
# <a name="d3dxrts_desc-structure"></a>D3DXRTS \_ DESC (estructura)

Describe una superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la superficie de representación, en píxeles.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de la superficie de representación, en píxeles.

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel de la superficie de representación.

</dd> <dt>

**Galería de detalles**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Si **es TRUE,** la superficie de representación admite una superficie de galería de símbolos de profundidad; De lo contrario, este miembro se establece **en FALSE.**

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Si DepthStencil se establece en **TRUE,** este parámetro es un miembro del tipo enumerado [D3DFORMAT,](d3dformat.md) que describe el formato de galería de símbolos de profundidad de la superficie de representación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface::GetDesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
