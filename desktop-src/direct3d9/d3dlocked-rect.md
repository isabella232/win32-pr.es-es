---
description: Describe una región rectangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT estructura (D3D9Types.h)
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
ms.openlocfilehash: b419483329e5461de5bc98b3a37b556e37138a055932b1d6c80d3a19b13ae516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988905"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ RECT (estructura)

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

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes de una fila de la superficie.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **\* void**

</dd> <dd>

Puntero a los bits bloqueados. Si se [**proporcionó un RECT**](/previous-versions//dd162897(v=vs.85)) a la llamada [**LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) los pBits se desplazarán adecuadamente desde el principio de la superficie.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El tono de los formatos DXTn es diferente de lo que se devolvió en DirectX 7. Ahora hace referencia al número de bytes de una fila de bloques. Por ejemplo, si tiene un ancho de 16, tendrá un tono de 4 bloques (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



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

 

 
