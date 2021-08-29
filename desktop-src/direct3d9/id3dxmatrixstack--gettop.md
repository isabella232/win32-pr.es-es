---
description: 'Método ID3DXMATRIXStack::GetTop (D3dx9math.h): recupera la matriz actual en la parte superior de la pila.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: Método ID3DXMATRIXStack::GetTop (D3dx9math.h)
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
ms.openlocfilehash: 2b2de5a846bdcc1296686011c8a176275a1c4a578bfbf2eff3a2c1ffe7af6efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095925"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::GetTop (D3dx9math.h)

Recupera la matriz actual en la parte superior de la pila.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Este método devuelve un puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que representa la matriz actual.

## <a name="remarks"></a>Comentarios

No se garantiza que el puntero [**D3DXMATRIX**](d3dxmatrix.md) devuelto por este método sea válido después de las operaciones de pila posteriores.

Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




