---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: Método ID3DXBaseEffect::GetParameter (D3DX9Shader.h)
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
ms.openlocfilehash: 37aa3ae609e20f80f354b33efbe2d0c771dc2c37d9709f4ce15898a4cf99f7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121958"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>Método ID3DXBaseEffect::GetParameter

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

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del parámetro o **NULL para** los parámetros de nivel superior. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del parámetro especificado o **NULL** si el índice no es válido. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
