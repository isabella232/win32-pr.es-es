---
description: Obtiene la transformación de la vista que se aplica a todos los sprites.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'ID3DX10Sprite:: GetViewTransform (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718559"
---
# <a name="id3dx10spritegetviewtransform-method"></a>ID3DX10Sprite:: GetViewTransform (método)

Obtiene la transformación de la vista que se aplica a todos los sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pViewTransform* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que se establecerá en la transformación del Sprite a partir del espacio universal original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

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

 

 
