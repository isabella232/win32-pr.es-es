---
title: Función ProcessTriTessFactorsAvg
description: Genera los factores de teselación corregidos para una revisión tri. | Función ProcessTriTessFactorsAvg
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- Función ProcessTriTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d119ee7011bbd4a03a2a2c8247b9df9e95f983e07ffd3ab3e4603a3a3eaa7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067775"
---
# <a name="processtritessfactorsavg-function"></a>Función ProcessTriTessFactorsAvg

Genera los factores de teselación corregidos para una revisión tri.

## <a name="syntax"></a>Sintaxis

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*RawEdgeFactors* \[ En\]
</dt> <dd>

Tipo: **float3**

Los factores de teselación del borde, pasados a la fase del teselador.

</dd> <dt>

*InsideScale* \[ En\]
</dt> <dd>

Tipo: **float**

Factor de escala aplicado a los factores de teselación UV calculados por la fase de teselación. El intervalo permitido para InsideScale es de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Tipo: **float3**

Factores de teselación de borde redondeados calculados por la fase del teselador.

</dd> <dt>

*RoundedInsideTessFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Factores de teselación calculados por la fase del teselador y redondeados.

</dd> <dt>

*UnroundedInsideTessFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Los factores de teselación UV originales, sin desenlazamiento, calculados por la fase de teselación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Genera los factores de teselación corregidos para una revisión tri, computando el factor de teselación interno como el promedio de los factores de teselación perimetral, que luego se escala mediante InsideScale. A continuación, el resultado se redondea en función del modo de creación de particiones, pero los resultados sin dividir están disponibles mediante el parámetro UnroundedInsideTessFactor.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




