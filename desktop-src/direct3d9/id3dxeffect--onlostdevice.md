---
description: Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'ID3DXEffect:: OnLostDevice (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af2d17c99f0b694a8b27924c34faa2a1f633fafb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707797"
---
# <a name="id3dxeffectonlostdevice-method"></a>ID3DXEffect:: OnLostDevice (método)

Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.

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

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9:: RESET**](/windows/desktop/api). Incluso si el dispositivo no se perdió realmente, **ID3DXEffect:: OnLostDevice** es responsable de liberar stateblocks y otros recursos que pueden ser necesarios para su lanzamiento antes de restablecer el dispositivo. Como resultado, el objeto Font no se puede volver a usar antes de llamar a **IDirect3DDevice9:: RESET** y después a [**ID3DXEffect:: OnResetDevice**](id3dxeffect--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




