---
title: D3DX_R16G16_FLOAT_to_FLOAT2 función
description: Desempaqueta los datos del sombreador DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB en XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- D3DX_R16G16_FLOAT_to_FLOAT2 function HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bb60ed211fa919c511a2061871ae47cd5eacaa29d37df7442939d0eedfb70a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855475"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a>Función D3DX \_ R16G16 \_ FLOAT \_ to \_ FLOAT2

Desempaqueta los datos del sombreador DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB en XMFLOAT2.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
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

 

 





