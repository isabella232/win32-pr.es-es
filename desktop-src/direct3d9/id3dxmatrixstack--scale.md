---
description: 'Método ID3DXMATRIXStack::Scale (D3dx9math.h): escale la matriz actual sobre el origen de la coordenada mundial.'
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: Método ID3DXMATRIXStack::Scale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565893"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::Scale (D3dx9math.h)

Escale la matriz actual sobre el origen de la coordenada mundial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Componente de escalado en la dirección X.

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Componente de escalado en la dirección Y.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Componente de escalado en dirección z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Observaciones

Este método multiplica a la derecha la matriz actual por la matriz de escala calculada. La transformación trata sobre el origen del mundo actual.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::ScaleLocal**](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
