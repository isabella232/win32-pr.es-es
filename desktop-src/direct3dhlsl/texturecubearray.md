---
title: Objeto TextureCubeArray
description: Tipo TextureCubeArray (tal como existe en el modelo de sombreador 4) más las variables de recurso. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- HLSL del objeto TextureCubeArray
- HLSL del objeto TextureCubeArray, descrito
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104997989"
---
# <a name="texturecubearray-object"></a>Objeto TextureCubeArray

Tipo **TextureCubeArray** ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **TextureCubeArray** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Recopilar**](texturecubearray-gather.md)                         | Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                          |
| [**Ejemplo**](texturecubearray-sample.md)                         | Muestrea una textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Muestrea una textura con un valor de comparación para rechazar ejemplos.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Muestrea una textura en el nivel de mipmap especificado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





