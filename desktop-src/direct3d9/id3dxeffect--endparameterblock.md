---
description: Detiene la captura de cambios de estado de parámetro de efecto.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect:: EndParameterBlock (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003836"
---
# <a name="id3dxeffectendparameterblock-method"></a>ID3DXEffect:: EndParameterBlock (método)

Detiene la captura de cambios de estado de parámetro de efecto.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador para el bloque de estado del parámetro.

## <a name="remarks"></a>Observaciones

Todos los parámetros de efecto que cambian el estado (después de llamar a BeginParameterBlock y antes de llamar a EndParameterBlock) se guardarán en un bloque de estado de parámetro de efecto. Use ApplyParameterBlock para aplicar este bloque de cambios de estado en el sistema de efectos. Una vez que haya terminado con un bloque de estado, use DeleteParameterBlock para liberar memoria.

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

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




