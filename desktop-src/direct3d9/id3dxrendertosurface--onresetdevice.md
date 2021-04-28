---
description: 'Método ID3DXRenderToSurface::OnResetDevice: use este método para volver a adquirir recursos y guardar el estado inicial.'
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: Método ID3DXRenderToSurface::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17af145a236d2b3a51d271c6687d78d81a387363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107193"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a>Método ID3DXRenderToSurface::OnResetDevice

Use este método para volver a adquirir recursos y guardar el estado inicial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar a ID3DXRenderToSurface::OnResetDevice cada vez que se restablezca el dispositivo (mediante [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)antes de llamar a cualquier otro método. Este es un buen lugar para volver a adquirir recursos de memoria de vídeo y capturar bloques de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
