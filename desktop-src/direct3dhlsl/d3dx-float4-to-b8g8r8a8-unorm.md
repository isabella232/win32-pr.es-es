---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM función)
description: Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM.
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986869"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a>D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ función UNORM

Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Datos del sombreador que se van a empaquetar.

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

 

 





