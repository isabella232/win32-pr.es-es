---
title: D3DX_R10G10B10A2_UNORM_to_FLOAT4 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R10G10B10A2 UNORM con formato DXGI en un XMFLOAT4.
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c93bd6fb9cce07ee13a873b4fade91bd322824
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987156"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a>D3DX \_ R10G10B10A2 \_ UNORM \_ a la \_ función FLOAT4

Desempaqueta los \_ datos del \_ \_ sombreador de R10G10B10A2 UNORM con formato DXGI en un XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
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

 

 





