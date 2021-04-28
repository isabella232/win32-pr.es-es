---
description: 'Método ID3DXRenderToSurface::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: Método ID3DXRenderToSurface::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093123"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a>Método ID3DXRenderToSurface::OnLostDevice

Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset). Incluso si el dispositivo no se perdió realmente, ID3DXRenderToSurface::OnLostDevice es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo. Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, ID3DXRenderToSurface::OnResetDevice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
