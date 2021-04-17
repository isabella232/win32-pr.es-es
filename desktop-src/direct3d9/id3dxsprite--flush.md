---
description: 'Obliga a que todos los sprites por lotes se envíen al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a ID3DXSprite:: Begin. A continuación, se borra la lista de sprites por lotes.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite:: Flush (método) (D3dx9core. h)'
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
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718290"
---
# <a name="id3dxspriteflush-method"></a>ID3DXSprite:: Flush (método)

Obliga a que todos los sprites por lotes se envíen al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). A continuación, se borra la lista de sprites por lotes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: end**](id3dxsprite--end.md)
</dt> </dl>

 

 




