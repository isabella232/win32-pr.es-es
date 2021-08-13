---
title: Objeto TextureCubeArray
description: Tipo TextureCubeArray (como existe en El modelo de sombreador 4) más variables de recursos. Este objeto de textura admite estos métodos además de los métodos de Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Objeto TextureCubeArray HLSL
- Objeto TextureCubeArray HLSL , descrito
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0b5687e26ebb8a80dbd75e5849ad95de29dacec90c64e660e59dce71c796b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786173"
---
# <a name="texturecubearray-object"></a>Objeto TextureCubeArray

**Tipo TextureCubeArray** ([tal y como existe en Shader Model 4](dx-graphics-hlsl-to-type.md)) más variables de recursos. Este objeto de textura admite estos métodos además de los métodos de Shader Model 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto TextureCubeArray** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texturecubearray-gather.md)                         | Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Devuelve los componentes azules de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve su comparación con un valor de comparación.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente alfa con un valor de comparación.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente azul con un valor de comparación.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente verde con un valor de comparación.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente rojo con un valor de comparación.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Devuelve los componentes rojos de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                          |
| [**Muestra**](texturecubearray-sample.md)                         | Muestrea una textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Muestrea una textura después de aplicar el valor de sesgo al nivel mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Muestrea una textura con un valor de comparación para rechazar muestras.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Muestrea una textura en el nivel de mapa mip especificado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





