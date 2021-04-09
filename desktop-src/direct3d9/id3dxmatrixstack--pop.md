---
description: Quita la matriz actual de la parte superior de la pila.
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: 'ID3DXMATRIXStack: método OP:P (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083710"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a>ID3DXMATRIXStack: método OP:P (D3dx9math. h)

Quita la matriz actual de la parte superior de la pila.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que este método reduce el número de elementos de la pila en 1, quitando de forma eficaz la matriz actual de la parte superior de la pila y promocionando una matriz a la parte superior de la pila. Si el recuento actual de elementos de la pila es 0, este método devuelve sin realizar ninguna acción. Si el recuento actual de elementos de la pila es 1, este método vacía la pila.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P uscripción**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




