---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda que no distinga mayúsculas de minúsculas.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect:: GetParameterBySemantic (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362775"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>ID3DXBaseEffect:: GetParameterBySemantic (método)

Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda que no distinga mayúsculas de minúsculas.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del parámetro o **null** para los parámetros de nivel superior. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre semántico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del primer parámetro que coincide con la semántica especificada, o **null** si no se encontró la semántica. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
