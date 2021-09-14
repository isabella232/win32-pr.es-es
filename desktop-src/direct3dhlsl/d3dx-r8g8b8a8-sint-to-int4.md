---
title: D3DX_R8G8B8A8_SINT_to_INT4 función
description: Desempaqueta los datos del sombreador SINT DXGI \_ FORMAT \_ R8G8B8A8 \_ en un XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4 función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360823"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a>Función D3DX \_ R8G8B8A8 \_ SINT \_ to \_ INT4

Desempaqueta los datos del sombreador SINT DXGI \_ FORMAT \_ R8G8B8A8 \_ en un XMINT4.

## <a name="syntax"></a>Sintaxis

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
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

 

 





