---
description: Establece una matriz de matrices no transpuestas.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: Método ID3DXTextureShader::SetMatrixArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f37d637833bb1b256b86f8bebf7879badc6730e91ae4fce7eecfdd1566d548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847025"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a>Método ID3DXTextureShader::SetMatrixArray

Establece una matriz de matrices no transpuestas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de matrices constantes. Vea [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz de matrices no transpuestas. Vea [**D3DXMATRIX.**](d3dxmatrix.md)

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de matrices de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Una matriz no transpuesta contiene datos principales de fila; es decir, cada vector está contenido en una fila.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
