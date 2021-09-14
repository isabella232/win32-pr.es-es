---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact función
description: Desempaqueta los datos del sombreador SRGB DXGI \_ FORMAT \_ B8G8R8X8 UNORM en \_ \_ XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact función
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact function HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264316"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>Función \_ \_ \_ \_ \_ \_ inexacta D3DX B8G8R8X8 UNORM SRGB to FLOAT3

Desempaqueta los datos del sombreador SRGB DXGI \_ FORMAT \_ B8G8R8X8 UNORM en \_ \_ XMFLOAT3.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Datos empaquetados del sombreador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos del sombreador desempaquetados.

## <a name="remarks"></a>Observaciones

Esta función usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión exacta de SRGB a float.

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

 

 





