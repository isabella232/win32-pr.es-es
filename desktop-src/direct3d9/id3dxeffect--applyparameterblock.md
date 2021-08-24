---
description: Aplique los valores de un bloque de estado al estado del sistema de efecto actual.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: Método ID3DXEffect::ApplyParameterBlock (D3DX9Effect.h)
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
ms.openlocfilehash: 8f5a382823da73df68ec0c32e120c0e94a2a7deba86e6aac4afe01e4e46acd7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951805"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>Método ID3DXEffect::ApplyParameterBlock

Aplique los valores de un bloque de estado al estado del sistema de efecto actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *hParameterBlock* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del bloque de parámetros. Este es el identificador devuelto por [**ID3DXEffect::EndParameterBlock.**](id3dxeffect--endparameterblock.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Capture los cambios de estado del parámetro de efecto en un bloque de parámetros mediante una llamada a BeginParameterBlock; detenga la captura de cambios de estado mediante una llamada a EndParameterBlock. Estos cambios de estado incluyen los cambios de parámetros de efecto que se producen dentro de una técnica (incluidos los que están fuera de un paso). Una vez que haya terminado con el bloque de parámetros, llame a DeleteParameterBlock para recuperar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



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

 

 




