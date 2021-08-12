---
description: Obliga a que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a ID3DXSprite::Begin. A continuación, se borra la lista de sprites por lotes.
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: Método ID3DXSprite::Flush (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766fbe41491fc6861ac3eaf366c3a858870c560139f1048d405184b580e72229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292697"
---
# <a name="id3dxspriteflush-method"></a>Método ID3DXSprite::Flush

Obliga a que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a [**ID3DXSprite::Begin**](id3dxsprite--begin.md). A continuación, se borra la lista de sprites por lotes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::End**](id3dxsprite--end.md)
</dt> </dl>

 

 




