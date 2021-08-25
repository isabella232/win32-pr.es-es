---
description: Describe un paso para un objeto de efecto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC estructura (D3dx9effect.h)
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
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894055"
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

Valor de cadena utilizado para el paso.

</dd> <dt>

**anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Vea [Agregar información para hacer efecto a los parámetros con \_ anotaciones](using-an-effect.md).

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntero a la función del sombreador de vértices. Si se crea un efecto con [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md), esta estructura devolverá un puntero **NULL** cuando [**getPassDesc**](id3dxbaseeffect--getpassdesc.md)lo llame.

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntero a la función de sombreador de píxeles. Si se crea un efecto con [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md), esta estructura devolverá un puntero **NULL** cuando [**getPassDesc**](id3dxbaseeffect--getpassdesc.md)lo llame.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
