---
description: Dibuje una matriz de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: Método ID3DX10Sprite::D rawSpritesImmediate (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0a3295d64efc3f3ff05b39e0866a15fb7eed9ba2d8c580fe2c7b219d36708e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046903"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>Método ID3DX10Sprite::D rawSpritesImmediate

Dibuje una matriz de sprites. Esto enviará inmediatamente los sprites al dispositivo para su representación, que es diferente de [**ID3DX10Sprite::D rawSpritesBuffered,**](id3dx10sprite-drawspritesbuffered.md) que solo agrega una matriz de sprites a un lote de sprites que se representarán cuando se llama a [**ID3DX10Sprite::Flush.**](id3dx10sprite-flush.md) Este método de dibujo es muy útil al dibujar un gran número de sprites que ya se han ordenado en la CPU (o no es necesario ordenar), como en un sistema de partículas. Se debe llamar a esto entre llamadas a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End**](id3dx10sprite-end.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSprites* \[ En\]
</dt> <dd>

Tipo: **[ **SPRITE D3DX10 \_**](d3dx10-sprite.md)\***

Matriz de sprites que se dibujarán. Consulte [**SPRITE D3DX10 \_**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de sprites en pSprites.

</dd> <dt>

*cbSprite* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

El tamaño de la estructura sprite que se pasa a pSprites. Pasar 0 equivale a pasar sizeof(D3DX10 \_ SPRITE).

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
