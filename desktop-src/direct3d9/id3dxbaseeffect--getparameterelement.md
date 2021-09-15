---
description: Obtiene el identificador de un parámetro de elemento de matriz.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: Método ID3DXBaseEffect::GetParameterElement (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566625"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>Método ID3DXBaseEffect::GetParameterElement

Obtiene el identificador de un parámetro de elemento de matriz.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de la matriz. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*ElementIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de elemento de matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del parámetro especificado o **NULL** si hParameter o ElementIndex no son válidos. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="remarks"></a>Observaciones

Este método se usa para obtener un elemento de un parámetro que es una matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
