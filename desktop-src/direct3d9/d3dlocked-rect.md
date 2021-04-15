---
description: Describe una región rectangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547966"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ Rect (estructura)

Describe una región rectangular bloqueada.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Inclinación**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes en una fila de la superficie.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Puntero a los bits bloqueados. Si se proporcionó un [**Rect**](/previous-versions//dd162897(v=vs.85)) a la llamada [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits se desplazará correctamente desde el inicio de la superficie.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El paso de los formatos DXTn es diferente de lo que se devolvió en DirectX 7. Ahora hace referencia al número de bytes de una fila de bloques. Por ejemplo, si tiene un ancho de 16, tendrá un paso de 4 bloques (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
