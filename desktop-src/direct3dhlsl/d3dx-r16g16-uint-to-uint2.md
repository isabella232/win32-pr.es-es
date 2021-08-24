---
title: D3DX_R16G16_UINT_to_UINT2 función
description: Desempaqueta los datos del sombreador UINT DXGI \_ FORMAT \_ R16G16 \_ en XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2 función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e2d31194364c865d8f6ae77a838e8f64f2c153b4185a8f3d26e32737835dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726915"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a>Función D3DX \_ R16G16 \_ UINT \_ a \_ UINT2

Desempaqueta los datos del sombreador UINT DXGI \_ FORMAT \_ R16G16 \_ en XMUINT2.

## <a name="syntax"></a>Sintaxis

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
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

 

 





