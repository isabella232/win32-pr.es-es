---
description: Establezca la transformación de la vista que se aplica a todos los sprites.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'ID3DX10Sprite:: SetViewTransform (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708125"
---
# <a name="id3dx10spritesetviewtransform-method"></a>ID3DX10Sprite:: SetViewTransform (método)

Establezca la transformación de la vista que se aplica a todos los sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pViewTransform* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a un D3DXMATRIX que contiene una transformación del objeto Sprite del espacio universal original. Use esta transformación para escalar, girar o transformar el sprite.

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

 

 
