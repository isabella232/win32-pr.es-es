---
description: 'Método ID3DXLine::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: Método ID3DXLine::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f67327a9582c959cc74d6bd2efb7f8d76dd6fac1e6de06d86aca28dfde5e3634
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951415"
---
# <a name="id3dxlineonlostdevice-method"></a>Método ID3DXLine::OnLostDevice

Use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/desktop/api). Aunque el dispositivo no se haya perdido realmente, **ID3DXLine::OnLostDevice** es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo. Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, [**ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 




