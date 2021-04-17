---
description: Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: 'ID3DXSprite:: OnLostDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f6b2b676e95b48f50b5c25a4bfc3a1bf3e7d610d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362627"
---
# <a name="id3dxspriteonlostdevice-method"></a>ID3DXSprite:: OnLostDevice (método)

Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9:: RESET**](/windows/desktop/api). Incluso si el dispositivo no se perdió realmente, **ID3DXSprite:: OnLostDevice** es responsable de liberar stateblocks y otros recursos que pueden ser necesarios para su lanzamiento antes de restablecer el dispositivo. Como resultado, el objeto Font no se puede volver a usar antes de llamar a **IDirect3DDevice9:: RESET** y después a [**ID3DXSprite:: OnResetDevice**](id3dxsprite--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




