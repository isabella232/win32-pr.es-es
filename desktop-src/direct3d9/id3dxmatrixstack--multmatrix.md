---
description: 'Método ID3DXMATRIXStack::MultMatrix (D3dx9math.h): determina el producto de la matriz actual y la matriz dada.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: Método ID3DXMATRIXStack::MultMatrix (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9d0808f1b23475b823ea43f55d93f8dacb01e4e491957fa34100110946fa72e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856465"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::MultMatrix (D3dx9math.h)

Determina el producto de la matriz actual y la matriz dada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMat* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que se va a multiplicar por la matriz actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método multiplica a la derecha la matriz dada a la matriz actual (la transformación trata sobre el origen del mundo actual).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Este método no agrega un elemento a la pila, reemplaza la matriz actual por el producto de la matriz actual y la matriz dada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




