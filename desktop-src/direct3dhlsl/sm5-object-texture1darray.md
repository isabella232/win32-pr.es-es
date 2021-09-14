---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888180"
---
# <a name="texture1darray"></a>Texture1DArray

Tipo Texture1DArray ([tal y como existe en Shader Model 4)](dx-graphics-hlsl-to-type.md)más variables de recursos. Este objeto de textura admite los métodos siguientes, además de los métodos del modelo de sombreador 4.



| Método                                                                       | Descripción                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Carga**](texture1darray-load.md)                                          | Lee los datos de textura.                                                                        |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Muestra**](texture1darray-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Muestrea una textura después de aplicar el valor de sesgo al nivel de mapa mip.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Muestrea una textura mediante un valor de comparación para rechazar muestras.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Muestrea una textura en el nivel de mapa mip especificado.                                           |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

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

 

 




