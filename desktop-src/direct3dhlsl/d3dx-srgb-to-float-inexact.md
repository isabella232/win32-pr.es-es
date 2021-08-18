---
title: D3DX_SRGB_to_FLOAT_inexact función
description: Convierte un valor SRGB en FLOAT. | D3DX_SRGB_to_FLOAT_inexact función
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact function HLSL
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
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515696"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>Función \_ \_ \_ \_ inexacta D3DX SRGB to FLOAT

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

Valor de SRGB que se debe convertir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de SRGB convertido.

## <a name="remarks"></a>Comentarios

Esta función no tiene una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa [**D3DX \_ SRGB \_ a \_ FLOAT**](d3dx-srgb-to-float.md) usa una tabla de búsqueda para proporcionar una conversión exacta de SRGB a float.

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

 

 





