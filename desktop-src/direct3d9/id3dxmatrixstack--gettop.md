---
description: Recupera la matriz actual en la parte superior de la pila.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack:: GetTop (método) (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717651"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>ID3DXMATRIXStack:: GetTop (método) (D3dx9math. h)

Recupera la matriz actual en la parte superior de la pila.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Este método devuelve un puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz actual.

## <a name="remarks"></a>Observaciones

No se garantiza que el puntero [**D3DXMATRIX**](d3dxmatrix.md) devuelto por este método sea válido después de las operaciones de pila posteriores.

Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P uscripción**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




