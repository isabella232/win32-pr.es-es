---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4 función
description: Desempaqueta los datos del \_ \_ sombreador DXGI FORMAT B8G8R8A8 \_ UNORM en XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4 function HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f82f827342cffbf34bde649a3e9a50f2fb42e7ef06b8bdd43a639298e6b0a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025055"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a>Función D3DX \_ B8G8R8A8 \_ UNORM \_ a \_ FLOAT4

Desempaqueta los datos del \_ \_ sombreador DXGI FORMAT B8G8R8A8 \_ UNORM en XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
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

 

 





