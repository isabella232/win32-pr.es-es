---
description: 'Método ID3DXTextureShader::SetIntArray: establece una matriz de enteros.'
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: Método ID3DXTextureShader::SetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ddc00637bddf2810e73be7755a9dcfb8696053e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970808"
---
# <a name="id3dxtextureshadersetintarray-method"></a>Método ID3DXTextureShader::SetIntArray

Establece una matriz de enteros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de constantes. Vea [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pn* \[ En\]
</dt> <dd>

Tipo: **const [**INT**](../winprog/windows-data-types.md) \***

Matriz de enteros.

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de enteros de la matriz.

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

 

 
