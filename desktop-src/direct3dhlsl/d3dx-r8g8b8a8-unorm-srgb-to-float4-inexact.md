---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact función
description: Desempaqueta los datos del sombreador DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB en XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact función
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede0d10bd8c90514771fa6520eb41e0bd555a3d969b230bb2932665ec0c81796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727350"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>Función \_ \_ \_ \_ \_ \_ inexacta D3DX R8G8B8A8 UNORM SRGB to FLOAT4

Desempaqueta los datos del sombreador DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB en XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

Datos del sombreador desempaquetar.

## <a name="remarks"></a>Comentarios

Esta función usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ a \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión exacta de SRGB a float.

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

 

 





