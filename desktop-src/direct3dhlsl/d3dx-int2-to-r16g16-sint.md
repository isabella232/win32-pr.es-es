---
title: D3DX_INT2_to_R16G16_SINT función)
description: Vuelve a empaquetar el XMINT2 determinado en un formato de DXGI \_ \_ R16G16 \_ Sint.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987187"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a>D3DX \_ INT2 \_ a \_ R16G16 \_ función Sint

Vuelve a empaquetar el XMINT2 determinado en un formato de DXGI \_ \_ R16G16 \_ Sint.

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
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

 

 





