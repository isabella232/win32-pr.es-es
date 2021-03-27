---
title: ddx_fine función)
description: Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla. | ddx_fine función)
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine de la función HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986755"
---
# <a name="ddx_fine-function"></a>\_función DDX Fine

Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla.

## <a name="syntax"></a>Sintaxis

``` syntax
float ddx_fine(
  in float value
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

El derivado parcial de precisión alta de *Value*.

## <a name="remarks"></a>Observaciones

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
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

 

 




