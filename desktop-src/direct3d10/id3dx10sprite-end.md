---
description: Llame a esto después de ID3DX10Sprite::Flush. Si se especificó D3DX10 SPRITE SAVE STATE cuando se llamó a ID3DX10Sprite::Begin, esta API restaurará el estado del dispositivo a como estaba antes de llamar a \_ \_ \_ ID3DX10Sprite::Begin.
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: Método ID3DX10Sprite::End (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02cfa1e92275230bd3a853aa9079187181089c46b4e4f193404b9dc0c709c9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302294"
---
# <a name="id3dx10spriteend-method"></a>Método ID3DX10Sprite::End

Llame a esto después de ID3DX10Sprite::Flush. Si se especificó D3DX10 SPRITE SAVE STATE cuando se llamó a ID3DX10Sprite::Begin, esta API restaurará el estado del dispositivo a como estaba antes de llamar a \_ \_ \_ ID3DX10Sprite::Begin.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




