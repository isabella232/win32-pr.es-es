---
description: Fuerce que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a ID3DX10Sprite::Begin. A continuación, se borra la lista de sprites por lotes.
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: Método ID3DX10Sprite::Flush (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d74c96ebab8b1e174a44124aaa53b714a9ea860fc9fa2ea5ae3e25c9779aae01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302248"
---
# <a name="id3dx10spriteflush-method"></a>Método ID3DX10Sprite::Flush

Fuerce que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a ID3DX10Sprite::Begin. A continuación, se borra la lista de sprites por lotes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

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

 

 




