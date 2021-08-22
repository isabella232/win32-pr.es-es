---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB función
description: Empaqueta el XMFLOAT3 especificado de nuevo en un DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB function HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e74519248f84890f29ebe9e00e02c76bce63775e938b40468041218025b0a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371335"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a>Función D3DX \_ FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM \_ SRGB

Empaqueta el XMFLOAT3 especificado de nuevo en un DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
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

[Desempaquetar y empaquetar DXGI \_ FORMAT In-Place edición de imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





