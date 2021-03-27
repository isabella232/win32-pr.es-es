---
title: ddy_coarse función)
description: Calcula un derivado parcial de precisión baja con respecto a la coordenada y del espacio de pantalla.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse de la función HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076882"
---
# <a name="ddy_coarse-function"></a>DDY \_ función gruesa

Calcula un derivado parcial de precisión baja con respecto a la coordenada y del espacio de pantalla.

## <a name="syntax"></a>Sintaxis

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **float**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float**

Derivado parcial de precisión baja de *Value*.

## <a name="remarks"></a>Observaciones

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




