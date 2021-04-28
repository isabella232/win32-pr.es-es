---
description: 'Método ID3DXTextureShader::GetConstant: obtiene una constante mediante la búsqueda de su índice.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Método ID3DXTextureShader::GetConstant (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117673"
---
# <a name="id3dxtextureshadergetconstant-method"></a>Método ID3DXTextureShader::GetConstant

Obtiene una constante mediante la búsqueda de su índice.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador [de](handles.md) la estructura de datos primaria. Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **NULL.**

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de base cero de la constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante.

## <a name="remarks"></a>Comentarios

Para obtener una constante de una matriz de constantes, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
