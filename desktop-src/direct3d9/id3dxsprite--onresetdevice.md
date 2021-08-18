---
description: 'Método ID3DXSprite::OnResetDevice: use este método para volver a adquirir recursos y guardar el estado inicial.'
ms.assetid: 74f8616e-c3ed-4231-b701-009213ea48c0
title: Método ID3DXSprite::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16086aca86e0df8c2c75e6a055be9fa95f7cc97259f37401aa932af962409811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800583"
---
# <a name="id3dxspriteonresetdevice-method"></a>Método ID3DXSprite::OnResetDevice

Use este método para volver a adquirir recursos y guardar el estado inicial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar **a ID3DXSprite::OnResetDevice** cada vez que se restablezca el dispositivo (mediante [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes de llamar a cualquier otro método. Este es un buen lugar para volver a adquirir recursos de memoria de vídeo y capturar bloques de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 
