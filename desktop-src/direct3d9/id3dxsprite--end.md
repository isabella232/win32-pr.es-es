---
description: 'Llama a ID3DXSprite:: Flush y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a ID3DXSprite:: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite:: end (método) (D3dx9core. h)'
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
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424452"
---
# <a name="id3dxspriteend-method"></a>ID3DXSprite:: end (método)

Llama a [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

**ID3DXSprite:: end** no se puede usar como sustituto de [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




