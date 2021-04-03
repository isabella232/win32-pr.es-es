---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect:: GetParameter (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083806"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>ID3DXBaseEffect:: GetParameter (método)

Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del parámetro o **null** para los parámetros de nivel superior. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del parámetro especificado, o **null** si el índice no era válido. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
