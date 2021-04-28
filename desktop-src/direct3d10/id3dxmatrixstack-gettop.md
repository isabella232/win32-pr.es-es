---
description: 'Método ID3DXMATRIXStack::GetTop (D3DX10.h): recupera la matriz actual en la parte superior de la pila.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: Método ID3DXMATRIXStack::GetTop (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108043"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Método ID3DXMATRIXStack::GetTop (D3DX10.h)

Recupera la matriz actual en la parte superior de la pila.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Este método devuelve un puntero a una estructura D3DXMATRIX que representa la matriz actual.

## <a name="remarks"></a>Comentarios

No se garantiza que el puntero D3DXMATRIX devuelto por este método sea válido después de las operaciones de pila posteriores.

Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
