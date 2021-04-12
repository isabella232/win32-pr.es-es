---
description: Dibuja una matriz de objetos Sprite.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite::D método rawSpritesImmediate (D3DX10. h)
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
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362823"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite::D método rawSpritesImmediate

Dibuja una matriz de objetos Sprite. Esto enviará inmediatamente los sprites al dispositivo para su representación, que es diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que solo agrega una matriz de sprites a un lote de sprites que se representará cuando se llame a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) . Este método draw es muy útil cuando se dibuja un gran número de sprites que ya se han ordenado en la CPU (o no es necesario ordenarlos), como en un sistema de partículas. Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).

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

*pSprites* \[ de\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***

Matriz de sprites que se va a dibujar. Vea [**D3DX10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de sprites en pSprites.

</dd> <dt>

*cbSprite* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño de la estructura de Sprite que se pasa a pSprites. Pasar 0 es el equivalente de pasar sizeof (D3DX10 \_ Sprite).

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Reservado.

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

 

 
