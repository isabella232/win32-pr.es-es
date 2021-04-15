---
description: Obtiene un puntero a la matriz de constantes de la tabla de constantes.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader:: GetConstantDesc (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708030"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>ID3DXTextureShader:: GetConstantDesc (método)

Obtiene un puntero a la matriz de constantes de la tabla de constantes.

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

*hConstant* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de una constante. Vea [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Devuelve un puntero a una matriz de descripciones. Vea [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

La entrada proporcionada debe ser el tamaño máximo de la matriz. El resultado es el número de elementos que se rellenan en la matriz cuando la función devuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Los muestreadores pueden aparecer más de una vez en una tabla de constantes; por lo tanto, este método puede devolver una matriz de descripciones con un índice de registro diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader::GetDesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
