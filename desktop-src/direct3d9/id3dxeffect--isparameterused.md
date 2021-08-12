---
description: Determina si la técnica usa un parámetro.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: Método ID3DXEffect::IsParameterUsed (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 80b0e69ec4f46541840d5b381cd25d056b25240a00a9ae84b0aaf46a79295ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296006"
---
# <a name="id3dxeffectisparameterused-method"></a>Método ID3DXEffect::IsParameterUsed

Determina si la técnica usa un parámetro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único del parámetro. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*hTechnique* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la técnica. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si se está utilizando el parámetro y devuelve **FALSE** si el parámetro no se está utilizando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
