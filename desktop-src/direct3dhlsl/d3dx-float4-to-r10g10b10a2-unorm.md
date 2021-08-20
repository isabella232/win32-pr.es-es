---
title: D3DX_FLOAT4_to_R10G10B10A2_UNORM función
description: Empaqueta el XMFLOAT4 especificado en un DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM function HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3303a419ffd5f53364aa509557832307f9014b1a37767c513b8b8c18900a687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516373"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a>Función \_ D3DX FLOAT4 \_ a \_ R10G10B10A2 \_ UNORM

Empaqueta el XMFLOAT4 especificado en un DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
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

 

 





