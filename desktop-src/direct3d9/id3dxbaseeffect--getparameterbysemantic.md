---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda sin distinción entre mayúsculas y minúsculas.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: Método ID3DXBaseEffect::GetParameterBySemantic (D3DX9Shader.h)
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
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791015"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>Método ID3DXBaseEffect::GetParameterBySemantic

Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda sin distinción entre mayúsculas y minúsculas.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del parámetro o **NULL para** los parámetros de nivel superior. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre semántico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del primer parámetro que coincide con la semántica especificada o **NULL** si no se encontró la semántica. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
