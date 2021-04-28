---
description: 'Método ID3DXTextureShader::GetConstantByName: obtiene una constante buscando su nombre.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: Método ID3DXTextureShader::GetConstantByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117663"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>Método ID3DXTextureShader::GetConstantByName

Obtiene una constante mediante la búsqueda de su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador [de](handles.md) la estructura de datos primaria. Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **NULL.**

</dd> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre de la constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
