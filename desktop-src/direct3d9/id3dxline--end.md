---
description: 'Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine:: end (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698376"
---
# <a name="id3dxlineend-method"></a>ID3DXLine:: end (método)

Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a [**ID3DXLine:: Begin**](id3dxline--begin.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

**ID3DXLine:: end** no se puede usar como sustituto de [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




