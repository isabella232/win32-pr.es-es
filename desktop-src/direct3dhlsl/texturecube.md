---
title: Objeto TextureCube
description: Tipo TextureCube (tal como existe en el modelo de sombreador 4) más las variables de recurso. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- HLSL del objeto TextureCube
- HLSL del objeto TextureCube, descrito
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104156984"
---
# <a name="texturecube-object"></a>Objeto TextureCube

Tipo **TextureCube** ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **TextureCube** tiene estos métodos.



| Método                                                      | Descripción                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Recopilar**](texturecube-gather.md)                         | Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.<br/>                                          |
| [**Ejemplo**](texturecube-sample.md)                         | Muestrea una textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Muestrea una textura con un valor de comparación para rechazar ejemplos.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Muestrea una textura en el nivel de mipmap especificado.<br/>                                                                                                    |



 

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

 

 





