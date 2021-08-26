---
description: Obtiene un puntero a la matriz de constantes de la tabla constante.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: Método ID3DXTextureShader::GetConstantDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8c7f65c9f2096339e0131d5d54c2fd65fb7e52849219f06f6a60fd44c518751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095675"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>Método ID3DXTextureShader::GetConstantDesc

Obtiene un puntero a la matriz de constantes de la tabla constante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de una constante. Vea [D3DXHANDLE.](d3dxfx.md)

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Devuelve un puntero a una matriz de descripciones. Vea [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

La entrada proporcionada debe ser el tamaño máximo de la matriz. La salida es el número de elementos que se rellenan en la matriz cuando se devuelve la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Los muestreadores pueden aparecer más de una vez en una tabla constante, por lo que este método puede devolver una matriz de descripciones cada una con un índice de registro diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader::GetDesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
