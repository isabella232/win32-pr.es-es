---
description: Describe un paso para un objeto de efecto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362429"
---
# <a name="d3dxpass_desc-structure"></a>D3DXPASS \_ DESC (estructura)

Describe un paso para un objeto de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de cadena usado para el paso.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntero a la función de sombreador de vértices. Si se crea un efecto con [D3DXFX \_ no \_ clonable](d3dxfx.md), esta estructura devolverá un puntero **nulo** cuando lo llame [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntero a la función de sombreador de píxeles. Si se crea un efecto con [D3DXFX \_ no \_ clonable](d3dxfx.md), esta estructura devolverá un puntero **nulo** cuando lo llame [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
