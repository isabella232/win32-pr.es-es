---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad13843dd74ab7cc188c3ab37d76df978f2a5fbd4bc6c292cfddfdf7c5841b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789382"
---
# <a name="texture2d"></a>Texture2D

Tipo Texture2D ([tal como existe en El modelo de sombreador 4)](dx-graphics-hlsl-to-type.md)más variables de recursos. Este objeto de textura admite los métodos siguientes, además de los métodos del modelo de sombreador 4.



| Método                                                                 | Descripción                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texture2d-gather.md)                                      | Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Devuelve los componentes rojos de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Devuelve los componentes azules de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve su comparación con un valor de comparación.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente verde con un valor de comparación. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente azul con un valor de comparación.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                                                                                       |
| [**Cargar**](texture2d-load.md)                                          | Lee los datos de textura.                                                                                                                                 |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Operator\[\]**](sm5-object-texture2d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                                                                                 |
| [**Muestra**](texture-sample-overload.md)                               | Muestrea una textura.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Muestrea una textura después de aplicar el valor de sesgo al nivel de mapa mip.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Muestrea una textura mediante un valor de comparación para rechazar muestras.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Muestrea una textura en el nivel de mapa mip especificado.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




