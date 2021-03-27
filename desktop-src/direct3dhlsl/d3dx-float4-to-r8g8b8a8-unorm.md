---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM función)
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821455"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a>D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ función UNORM

Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
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

 

 





