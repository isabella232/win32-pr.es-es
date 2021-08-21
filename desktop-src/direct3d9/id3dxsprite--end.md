---
description: Llama a ID3DXSprite::Flush y restaura el estado del dispositivo en el modo en que estaba antes de llamar a ID3DXSprite::Begin.
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: Método ID3DXSprite::End (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeade03ea423d08e412fe35f7c710c9d449cd74c3ed742627ed62954c6011f0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094128"
---
# <a name="id3dxspriteend-method"></a>Método ID3DXSprite::End

Llama [**a ID3DXSprite::Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo en el modo en que estaba antes de llamar a [**ID3DXSprite::Begin.**](id3dxsprite--begin.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

**ID3DXSprite::End** no se puede usar como sustituto de [**IDirect3DDevice9::EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




