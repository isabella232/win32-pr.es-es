---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM función
description: Empaqueta el XMFLOAT4 especificado de nuevo en UN DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM function HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0382cc5e7bfc47b8046eec437cbc25cf559c9116b4e6215cce9a3fb8f344f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286733"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>Función D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ SNORM

Empaqueta el XMFLOAT4 especificado de nuevo en UN DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Datos del sombreador que se empaquetan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos empaquetados del sombreador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones](format-conversion-functions.md)
</dt> <dt>

[Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





