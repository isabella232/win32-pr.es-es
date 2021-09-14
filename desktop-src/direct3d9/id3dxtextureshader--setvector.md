---
description: 'Método ID3DXTextureShader::SetVector: establece un vector 4D.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: Método ID3DXTextureShader::SetVector (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e917e4ff13cf7c03de264542dc1995364f1dc526
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888377"
---
# <a name="id3dxtextureshadersetvector-method"></a>Método ID3DXTextureShader::SetVector

Establece un vector 4D.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la constante de vector. Vea [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pVector* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a un vector 4D. Vea [**D3DXVECTOR4**](d3dxvector4.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




