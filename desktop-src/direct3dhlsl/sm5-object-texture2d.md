---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- HLSL de Texture2D
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104986167"
---
# <a name="texture2d"></a>Texture2D

Tipo Texture2D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.



| Método                                                                 | Descripción                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Recopilar**](texture2d-gather.md)                                      | Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                                                                                       |
| [**Carga**](texture2d-load.md)                                          | Lee los datos de textura.                                                                                                                                 |
| [**MIPS. Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Ejemplo**](texture-sample-overload.md)                               | Muestrea una textura.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Muestrea una textura con un valor de comparación para rechazar ejemplos.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Muestrea una textura en el nivel de mipmap especificado.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

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

 

 




