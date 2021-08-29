---
description: 'Método ID3DXMATRIXStack::P ush (D3dx9math.h): agrega una matriz a la pila.'
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: Método ID3DXMATRIXStack::P ush (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1211469b3b7cf90e9ddae1fd8edb51bb38d35b427f6cdf62684aa84142a77009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563945"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::P ush (D3dx9math.h)

Agrega una matriz a la pila.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Push();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método incrementa el recuento de elementos en la pila en 1, duplicando la matriz actual. La pila crecerá dinámicamente a medida que se agregan más elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




