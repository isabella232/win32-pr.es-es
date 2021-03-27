---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB función)
description: Empaqueta el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280446"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ UNORM \_ sRGB function

Empaqueta el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB uint.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Datos del sombreador desempaquetado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos del sombreador empaquetado.

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

 

 





