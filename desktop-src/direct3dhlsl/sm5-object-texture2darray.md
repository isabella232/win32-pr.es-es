---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab6e5c0a500a9f34cbd4e418a35e96687650f3df863e1fe77576c66ade718e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023405"
---
# <a name="texture2darray"></a>Texture2DArray

Tipo Texture2DArray ([tal como existe en El modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más variables de recursos. Este objeto de textura admite los métodos siguientes, además de los métodos del modelo de sombreador 4.



| Método                                                                      | Descripción                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texture2darray-gather.md)                                      | Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Devuelve los componentes rojos de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Devuelve los componentes azules de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve su comparación con un valor de comparación.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente verde con un valor de comparación. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente azul con un valor de comparación.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                                                                                       |
| [**Cargar**](texture2darray-load.md)                                          | Lee los datos de textura.                                                                                                                                 |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2darray-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Muestra**](texture2darray-sample.md)                                      | Muestrea una textura.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Muestrea una textura después de aplicar el valor de sesgo al nivel de mapa mip.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Muestrea una textura mediante un valor de comparación para rechazar muestras.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Muestrea una textura en el nivel de mapa mip especificado.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




