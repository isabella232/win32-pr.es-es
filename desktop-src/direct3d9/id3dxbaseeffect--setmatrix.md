---
description: 'Método ID3DXBaseEffect::SetMatrix: establece una matriz no transpuesta.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: Método ID3DXBaseEffect::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 77aad0573aed5e7dcb37ea82052b535badf8ee77d438393ad8d45e4963b79609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749015"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a>Método ID3DXBaseEffect::SetMatrix

Establece una matriz no transpuesta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una matriz sin transacciones. Vea [**D3DXMATRIX.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Una matriz no transpuesta contiene datos principales de fila. En otras palabras, cada vector se encuentra en una fila.

Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrix**](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




