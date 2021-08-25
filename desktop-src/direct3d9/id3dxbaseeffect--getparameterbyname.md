---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura mediante la búsqueda de su nombre.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: Método ID3DXBaseEffect::GetParameterByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 30a1e585cbbbaee4891e3e7dc2cd4e3d3c871fd33fe36daa51c9137c26bfdc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848685"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a>Método ID3DXBaseEffect::GetParameterByName

Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura mediante la búsqueda de su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del parámetro o **NULL para** los parámetros de nivel superior. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del parámetro especificado o **NULL** si el índice no era válido. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
