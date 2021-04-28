---
description: 'Método ID3DXMATRIXStack::P op (D3DX10.h): quita la matriz actual de la parte superior de la pila.'
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: Método ID3DXMATRIXStack::P op (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107933"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a>Método ID3DXMATRIXStack::P op (D3DX10.h)

Quita la matriz actual de la parte superior de la pila.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que este método reduce el número de elementos de la pila en 1, quitando eficazmente la matriz actual de la parte superior de la pila y promocionando una matriz en la parte superior de la pila. Si el recuento actual de elementos de la pila es 0, este método devuelve sin realizar ninguna acción. Si el recuento actual de elementos de la pila es 1, este método vacía la pila.

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

 

 




