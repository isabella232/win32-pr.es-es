---
description: Restaura el estado del dispositivo a la forma en que estaba cuando se llamó a ID3DXLine::Begin.
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: Método ID3DXLine::End (D3dx9core.h)
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
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987235"
---
# <a name="id3dxlineend-method"></a>Método ID3DXLine::End

Restaura el estado del dispositivo a la forma en que estaba cuando se llamó a [**ID3DXLine::Begin.**](id3dxline--begin.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

**ID3DXLine::End** no se puede usar como sustituto de [**IDirect3DDevice9::EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




