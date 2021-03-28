---
title: ProcessQuadTessFactorsMax función)
description: Genera los factores de teselación corregidos para una revisión cuádruple. | ProcessQuadTessFactorsMax función)
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- ProcessQuadTessFactorsMax de función HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62219301e93bebf7825328fd381b5d2fbb607925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986562"
---
# <a name="processquadtessfactorsmax-function"></a>ProcessQuadTessFactorsMax función)

Genera los factores de teselación corregidos para una revisión cuádruple.

## <a name="syntax"></a>Sintaxis

``` syntax
void ProcessQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*RawEdgeFactors* \[ de\]
</dt> <dd>

Tipo: **FLOAT4**

Factores de teselación perimetral que se pasan a la fase del teselador.

</dd> <dt>

*InsideScale* \[ de\]
</dt> <dd>

Tipo: **float**

Factor de escala aplicado a los factores de teselación de UV calculados por la fase de teselación. El intervalo permitido para InsideScale es de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ enuncia\]
</dt> <dd>

Tipo: **FLOAT4**

Los factores de teselación perimetral redondeados calculados por la fase del teselador.

</dd> <dt>

*RoundedInsideTessFactors* \[ enuncia\]
</dt> <dd>

Tipo: **float2**

Los factores de teselación redondeados calculados por la fase del teselador para los bordes interiores.

</dd> <dt>

*UnroundedInsideTessFactors* \[ enuncia\]
</dt> <dd>

Tipo: **float2**

Los factores de teselación calculados por la fase del teselador para los bordes interiores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Genera los factores de teselación corregidos para una revisión cuádruple, calculando los factores de teselación interiores como el máximo de los factores de teselación perimetral. Los factores Tess internos serán valores idénticos determinados por el máximo de los cuatro bordes escalados por InsideScale. Después, el resultado se redondea según el modo de partición, pero los resultados no redondeados están disponibles mediante el parámetro *UnroundedInsideTessFactors* .

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




