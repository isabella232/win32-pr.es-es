---
description: Obtiene una matriz transpuesta.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'ID3DXBaseEffect:: GetMatrixTranspose (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362777"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a>ID3DXBaseEffect:: GetMatrixTranspose (método)

Obtiene una matriz transpuesta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Devuelve una matriz transpuesta. Vea [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.

Si la matriz de destino es mayor que la matriz de origen, solo se rellenarán los elementos de la parte superior izquierda de la matriz de destino y los demás componentes de la matriz de destino se establecerán en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




