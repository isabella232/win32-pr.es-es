---
description: Agregue una matriz de sprites al lote de sprites que se va a representar.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite::D método rawSpritesBuffered (D3DX10. h)
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
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718562"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite::D método rawSpritesBuffered

Agregue una matriz de sprites al lote de sprites que se va a representar. Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md), y se debe llamar a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) antes de que finalice el envío de todos los sprites por lotes al dispositivo para su representación. Este método draw es muy útil cuando se dibuja un número pequeño de sprites que se desea almacenar en el búfer en un lote grande, como las fuentes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSprites* \[ de\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***

Matriz de sprites que se va a dibujar. Vea [**D3DX10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de sprites en pSprites.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
