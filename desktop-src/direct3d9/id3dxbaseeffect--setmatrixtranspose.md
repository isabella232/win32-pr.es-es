---
description: 'Método ID3DXBaseEffect::SetMatrixTranspose: establece una matriz transpuesta.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: Método ID3DXBaseEffect::SetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d516d9fc5a92ff3661caaf5fbca17372804ea2805688542a0283736cf55f4959
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790675"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a>Método ID3DXBaseEffect::SetMatrixTranspose

Establece una matriz transpuesta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrixTranspose(
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

Puntero a una matriz transpuesta. Vea [**D3DXMATRIX.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Una matriz transpuesta contiene datos principales de columna; es decir, cada vector se encuentra en una columna.

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

[**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




