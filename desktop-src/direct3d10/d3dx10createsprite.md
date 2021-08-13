---
description: Cree un sprite para dibujar una textura 2D. Nota En lugar de usar esta función, se recomienda usar Direct2D y la biblioteca DirectXTK, clase SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Función D3DX10CreateSprite (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f67a0a6e0be8a3ea71ff1eef46d72b6cf080d028e7cc32f72a52db6a209cea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541068"
---
# <a name="d3dx10createsprite-function"></a>Función D3DX10CreateSprite

Cree un sprite para dibujar una textura 2D.

> [!Note]  
> En lugar de usar esta función, se recomienda usar [Direct2D](../direct2d/direct2d-portal.md) y la biblioteca [DirectXTK,](https://github.com/Microsoft/DirectXTK) **clase SpriteBatch.**

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo (consulte [**ID3D10Device Interface)**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)que dibujará el sprite.

</dd> <dt>

*cDeviceBufferSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

El tamaño del búfer de vértices, en número de sprites, que se enviará al dispositivo cuando se llame a [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawSpritesImmediate.**](id3dx10sprite-drawspritesimmediate.md) Debe ser un número pequeño si sabe que va a representar un pequeño número de sprites a la vez (para ahorrar memoria) y un número grande si sabe que va a representar un gran número de sprites a la vez. El valor máximo es 4096. Si se especifica 0, el tamaño del búfer de vértices se establecerá automáticamente en 4096.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Dirección de un puntero a una interfaz sprite (vea [**ID3DX10Sprite Interface**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
