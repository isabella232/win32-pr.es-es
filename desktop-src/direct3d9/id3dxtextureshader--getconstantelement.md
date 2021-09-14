---
description: Obtenga una constante de la tabla constante.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: Método ID3DXTextureShader::GetConstantElement (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964736"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>Método ID3DXTextureShader::GetConstantElement

Obtenga una constante de la tabla constante.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador [de](handles.md) la matriz de constantes. Este valor puede no ser **NULL.**

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de base cero del elemento de la tabla constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante.

## <a name="remarks"></a>Observaciones

Para obtener una constante que no forma parte de una matriz, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) o [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
