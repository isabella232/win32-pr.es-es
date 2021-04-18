---
description: Aplique los valores de un bloque de estado al estado del sistema de efecto actual.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect:: ApplyParameterBlock (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718244"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>ID3DXEffect:: ApplyParameterBlock (método)

Aplique los valores de un bloque de estado al estado del sistema de efecto actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *hParameterBlock* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del bloque de parámetros. Este es el identificador devuelto por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Captura los cambios de estado de parámetro de efecto en un bloque de parámetros mediante una llamada a BeginParameterBlock; Detenga la captura de los cambios de estado llamando a EndParameterBlock. Estos cambios de estado incluyen cualquier cambio de parámetro de efecto que se produce dentro de una técnica (incluidos los que se encuentran fuera de un paso). Una vez que haya terminado con el bloque de parámetros, llame a DeleteParameterBlock para recuperar memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




