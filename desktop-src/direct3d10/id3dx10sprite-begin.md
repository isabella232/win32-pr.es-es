---
description: Preparar un dispositivo para dibujar sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite:: Begin (método) (D3DX10. h)'
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
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280412"
---
# <a name="id3dx10spritebegin-method"></a>ID3DX10Sprite:: Begin (método)

Preparar un dispositivo para dibujar sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Marcas que controlan cómo se dibujarán los sprites. Vea [**D3DX10 \_ Sprite \_ Flag**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Cada llamada a Begin debe coincidir con una llamada a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).

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

 

 
