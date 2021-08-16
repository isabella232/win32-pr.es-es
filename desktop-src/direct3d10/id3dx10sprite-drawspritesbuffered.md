---
description: Agregue una matriz de sprites al lote de sprites que se va a representar.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: Método ID3DX10Sprite::D rawSpritesBuffered (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bee3fd9344e393d2b5b9ddf6162286507fac918ea15f9abde2abcc2f80a5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540042"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>Método ID3DX10Sprite::D rawSpritesBuffered

Agregue una matriz de sprites al lote de sprites que se va a representar. Se debe llamar a esto entre llamadas a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End,**](id3dx10sprite-end.md)y se debe llamar a [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) antes de End para enviar todos los sprites por lotes al dispositivo para su representación. Este método de dibujo es más útil al dibujar un pequeño número de sprites que desea almacenar en búfer en un lote grande, como fuentes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSprites* \[ En\]
</dt> <dd>

Tipo: **[ **SPRITE D3DX10 \_**](d3dx10-sprite.md)\***

Matriz de sprites que se dibujarán. Consulte [**SPRITE D3DX10. \_**](d3dx10-sprite.md)

</dd> <dt>

*cSprites* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de sprites en pSprites.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

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

 

 
