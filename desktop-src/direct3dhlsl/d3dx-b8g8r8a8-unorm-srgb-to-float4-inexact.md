---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función)
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998304"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto (función)

Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Datos del sombreador empaquetado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos del sombreador desempaquetado.

## <a name="remarks"></a>Observaciones

Esta función usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta. La función alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa una tabla de búsqueda almacenada en el sombreador para dar una conversión de sRGB a Float exacta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. INL</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones](format-conversion-functions.md)
</dt> <dt>

[Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





