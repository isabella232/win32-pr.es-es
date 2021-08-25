---
title: ddx_coarse función
description: Calcula un derivado parcial de precisión baja con respecto a la coordenada x del espacio de pantalla.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse hlsl
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5521da56804156485fcacb37b43cbf27d8d4b3659cbced918eaea2c12b308ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855375"
---
# <a name="ddx_coarse-function"></a>Función general \_ ddx

Calcula un derivado parcial de precisión baja con respecto a la coordenada x del espacio de pantalla.

## <a name="syntax"></a>Sintaxis

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **float**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float**

Derivado parcial de precisión baja del *valor*.

## <a name="remarks"></a>Comentarios

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




