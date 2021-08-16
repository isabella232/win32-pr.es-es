---
title: Función Process2DQuadTessFactorsMax
description: Genera los factores de teselación corregidos para una revisión cuadrántica. | Función Process2DQuadTessFactorsMax
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Función HLSL process2DQuadTessFactorsMax
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f3325f08d1457230f52a539eaa9a7694d56266b7f2fd8cfd921c7a70e61ab568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510950"
---
# <a name="process2dquadtessfactorsmax-function"></a>Función Process2DQuadTessFactorsMax

Genera los factores de teselación corregidos para una revisión cuadrántica.

## <a name="syntax"></a>Sintaxis

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
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

Los factores de teselación del borde, pasados a la fase del teselador.

</dd> <dt>

*InsideScale* \[ En\]
</dt> <dd>

Tipo: **float2**

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

## <a name="remarks"></a>Comentarios

Genera los factores de teselación corregidos para una revisión cuadrántica y computa los factores de teselación dentro como el máximo de los factores de teselación perimetral. El usuario y la V dentro de los factores de teselación se calculan de forma independiente con los valores máximos de los lados opuestos del dominio y, a continuación, InsideScale los escala. A continuación, el resultado se redondea en función del modo de creación de particiones, pero los resultados sin dividir están disponibles mediante el parámetro UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




