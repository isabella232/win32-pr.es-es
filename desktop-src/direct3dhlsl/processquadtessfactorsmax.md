---
title: Función ProcessQuadTessFactorsMax
description: Genera los factores de teselación corregidos para una revisión cuadrántica. | Función ProcessQuadTessFactorsMax
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- Función HLSL de ProcessQuadTessFactorsMax
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884217"
---
# <a name="processquadtessfactorsmax-function"></a>Función ProcessQuadTessFactorsMax

Genera los factores de teselación corregidos para una revisión cuadrántica.

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

*RawEdgeFactors* \[ En\]
</dt> <dd>

Tipo: **float4**

Los factores de teselación del borde, que se pasan a la fase del teselador.

</dd> <dt>

*InsideScale* \[ En\]
</dt> <dd>

Tipo: **float**

Factor de escala aplicado a los factores de teselación UV calculados por la fase de teselación. El intervalo permitido para InsideScale es de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Tipo: **float4**

Factores de teselación de borde redondeados calculados por la fase del teselador.

</dd> <dt>

*RoundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Factores de teselación redondeados calculados por la fase del teselador para los bordes interiores.

</dd> <dt>

*UnroundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Factores de teselación calculados por la fase del teselador para los bordes interiores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Genera los factores de teselación corregidos para una revisión cuadrántica y computa los factores de teselación interno como el máximo de los factores de teselación perimetral. Los factores de tess interno serán valores idénticos determinados por el máximo de los cuatro bordes escalados por InsideScale. A continuación, el resultado se redondea según el modo de creación de particiones, pero los resultados sin dividir están disponibles mediante el parámetro *UnroundedInsideTessFactors.*

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




