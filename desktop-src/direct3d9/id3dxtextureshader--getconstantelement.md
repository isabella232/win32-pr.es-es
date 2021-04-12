---
description: Obtiene una constante de la tabla de constantes.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader:: GetConstantElement (método) (D3DX9Shader. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280347"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>ID3DXTextureShader:: GetConstantElement (método)

Obtiene una constante de la tabla de constantes.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Identificador](handles.md) de la matriz de constantes. Este valor no puede ser **null**.

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base cero del elemento de la tabla Constant.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante.

## <a name="remarks"></a>Observaciones

Para obtener una constante que no forma parte de una matriz, use [**ID3DXTextureShader:: GetConstant**](id3dxtextureshader--getconstant.md) o [**ID3DXTextureShader:: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
