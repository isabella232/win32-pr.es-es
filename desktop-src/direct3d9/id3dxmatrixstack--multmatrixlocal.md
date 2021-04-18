---
description: Determina el producto de la matriz especificada y la matriz actual.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'ID3DXMATRIXStack:: MultMatrixLocal (método) (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717647"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>ID3DXMATRIXStack:: MultMatrixLocal (método) (D3dx9math. h)

Determina el producto de la matriz especificada y la matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMat* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que se va a multiplicar por la matriz actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método multiplica la matriz especificada a la matriz actual (la transformación es sobre el origen local del objeto).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Este método no agrega un elemento a la pila, reemplaza la matriz actual con el producto de la matriz especificada y la matriz actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




