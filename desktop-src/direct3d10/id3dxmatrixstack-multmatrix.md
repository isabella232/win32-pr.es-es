---
description: 'Método ID3DXMATRIXStack::MultMatrix (D3DX10.h): determina el producto de la matriz actual y la matriz dada.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: Método ID3DXMATRIXStack::MultMatrix (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f881e3df820df87ea948893277950bce3ca289b8f9e0dcc6a4d34d46cca463ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736084"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>Método ID3DXMATRIXStack::MultMatrix (D3DX10.h)

Determina el producto de la matriz actual y la matriz dada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura D3DXMATRIX que se va a multiplicar por la matriz actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método multiplica a la derecha la matriz dada a la matriz actual (la transformación trata sobre el origen del mundo actual).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Este método no agrega un elemento a la pila, reemplaza la matriz actual por el producto de la matriz actual y la matriz dada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
