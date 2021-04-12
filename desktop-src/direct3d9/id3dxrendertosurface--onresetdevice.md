---
description: Use este método para volver a adquirir recursos y guardar el estado inicial.
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: 'ID3DXRenderToSurface:: OnResetDevice (método) (D3dx9core. h)'
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
ms.openlocfilehash: 09d8e3d2c7b628d36fee12525e9423059a7bd63a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362537"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a>ID3DXRenderToSurface:: OnResetDevice (método)

Use este método para volver a adquirir recursos y guardar el estado inicial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Se debe llamar a ID3DXRenderToSurface:: OnResetDevice cada vez que se restablezca el dispositivo (mediante [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes de que se llame a cualquier otro método. Este es un buen lugar para volver a adquirir recursos de memoria de vídeo y capturar bloques de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
