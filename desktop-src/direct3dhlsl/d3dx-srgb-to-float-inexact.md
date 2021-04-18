---
title: D3DX_SRGB_to_FLOAT_inexact función)
description: Convierte un valor SRGB en FLOAT. | D3DX_SRGB_to_FLOAT_inexact función)
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986881"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRGB \_ a \_ float \_ inexacto (función)

Convierte un valor SRGB en FLOAT.

## <a name="syntax"></a>Sintaxis

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Val* 
</dt> <dd>

Valor SRGB que se va a convertir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor SRGB convertido.

## <a name="remarks"></a>Observaciones

Esta función no tiene una precisión lo suficientemente alta como para proporcionar la respuesta exacta. La función alternativa de [**D3DX \_ sRGB \_ a \_ float**](d3dx-srgb-to-float.md) usa una tabla de búsqueda para proporcionar una conversión de sRGB a Float exacta.

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

 

 





