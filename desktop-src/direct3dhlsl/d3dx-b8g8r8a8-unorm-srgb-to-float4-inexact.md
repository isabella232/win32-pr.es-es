---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función
description: Desempaqueta los datos del sombreador SRGB DXGI \_ FORMAT \_ B8G8R8A8 UNORM en \_ \_ XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b6fc32a06ff436046de76e212ef8f90a06338a55caa285865f12c98d6d4b068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793889"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>Función inexacta D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ \_ to FLOAT4 \_

Desempaqueta los datos del sombreador SRGB DXGI \_ FORMAT \_ B8G8R8A8 UNORM en \_ \_ XMFLOAT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

Datos del sombreador desempaquetados.

## <a name="remarks"></a>Comentarios

Esta función usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión exacta de SRGB a float.

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

 

 





