---
title: D3DX_UINT4_to_R8G8B8A8_UINT función
description: Empaqueta el XMUINT4 especificado de nuevo en un UINT DXGI \_ FORMAT \_ R8G8B8A8. \_
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- D3DX_UINT4_to_R8G8B8A8_UINT function HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2185a28e094af06a25581152b9620e21446e614ed7b187bf2365fc912078ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727279"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a>Función \_ UINT de D3DX UINT4 \_ a \_ R8G8B8A8 \_

Empaqueta el XMUINT4 especificado de nuevo en un UINT DXGI \_ FORMAT \_ R8G8B8A8. \_

## <a name="syntax"></a>Sintaxis

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Datos del sombreador que se empaquetan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos empaquetados del sombreador.

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

 

 





