---
description: Prepare un dispositivo para dibujar sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: Método ID3DX10Sprite::Begin (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e23ff3e4b8be62ac97f2874aa398770936bd84ab1c330c94efb87146046db847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302410"
---
# <a name="id3dx10spritebegin-method"></a>Método ID3DX10Sprite::Begin

Prepare un dispositivo para dibujar sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Marcas que controlan cómo se dibujarán los sprites. Vea [**D3DX10 \_ SPRITE \_ FLAG**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Cada llamada a Begin debe coincidir con una llamada a [**ID3DX10Sprite::End**](id3dx10sprite-end.md).

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

 

 
