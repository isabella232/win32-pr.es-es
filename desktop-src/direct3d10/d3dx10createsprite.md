---
description: Cree un Sprite para dibujar una textura 2D. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar Direct2D y la biblioteca DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Función D3DX10CreateSprite (D3DX10. h)
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
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707807"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite función)

Cree un Sprite para dibujar una textura 2D.

> [!Note]  
> En lugar de usar esta función, se recomienda usar [Direct2D](../direct2d/direct2d-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.

 

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que va a dibujar el sprite.

</dd> <dt>

*cDeviceBufferSize* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño del búfer de vértices, en número de sprites, que se enviará al dispositivo cuando se llame a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) . Debe ser un número pequeño si sabe que va a representar un pequeño número de sprites a la vez (para ahorrar memoria) y un número grande si sabe que va a representar un gran número de objetos Sprite a la vez. El valor máximo es 4096. Si se especifica 0, el tamaño del búfer de vértices se establecerá automáticamente en 4096.

</dd> <dt>

*ppSprite* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

La dirección de un puntero a una interfaz de Sprite (vea la [**interfaz ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
