---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM función
description: Empaqueta el XMFLOAT3 especificado en un UINT DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM function HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee8da37854e78abb09e8d6781453d47cf3abed43847a96fe09b7d637e52ca429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516383"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a>Función \_ D3DX FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM

Empaqueta el XMFLOAT3 especificado en un UINT DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Datos del sombreador desempaquetados.

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

 

 





