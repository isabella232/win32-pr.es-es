---
description: Obtiene una matriz de matrices no transaccionadas.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: Método ID3DXBaseEffect::GetMatrixArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964815"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a>Método ID3DXBaseEffect::GetMatrixArray

Obtiene una matriz de matrices no transaccionadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pMatrix* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Devuelve una matriz de matrices no transpuestas. Vea [**D3DXMATRIX.**](d3dxmatrix.md)

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de matrices de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Una matriz no transaccional contiene datos principales de fila; es decir, cada vector está contenido en una fila.

Si las matrices de destino son mayores que las matrices de origen, solo se rellenarán los componentes superiores izquierdos de cada matriz de destino y los componentes restantes de la matriz de destino se establecerán en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
