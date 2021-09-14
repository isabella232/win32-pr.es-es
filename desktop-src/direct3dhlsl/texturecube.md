---
title: Objeto TextureCube
description: Tipo TextureCube (tal como existe en El modelo de sombreador 4) más variables de recursos. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Objeto TextureCube HLSL
- Objeto TextureCube HLSL , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888124"
---
# <a name="texturecube-object"></a>Objeto TextureCube

**Tipo TextureCube** ([tal y como existe en El modelo de sombreador 4)](dx-graphics-hlsl-to-type.md)más variables de recursos. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto TextureCube** tiene estos métodos.



| Método                                                      | Descripción                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texturecube-gather.md)                         | Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Devuelve los componentes azules de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve su comparación con un valor de comparación.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente azul con un valor de comparación.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente verde con un valor de comparación.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Devuelve los componentes rojos de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.<br/>                                          |
| [**Muestra**](texturecube-sample.md)                         | Muestrea una textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Muestrea una textura después de aplicar el valor de sesgo al nivel de mapa mip.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Muestrea una textura mediante un valor de comparación para rechazar muestras.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Muestrea una textura en el nivel de mapa mip especificado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





