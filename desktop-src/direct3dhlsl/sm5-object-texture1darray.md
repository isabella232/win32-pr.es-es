---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- HLSL de Texture1DArray
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076860"
---
# <a name="texture1darray"></a>Texture1DArray

Tipo Texture1DArray ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.



| Método                                                                       | Descripción                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Carga**](texture1darray-load.md)                                          | Lee los datos de textura.                                                                        |
| [**MIPS. Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Operador\[\]**](sm5-object-texture1darray-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Ejemplo**](texture1darray-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Muestrea una textura con un valor de comparación para rechazar ejemplos.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Muestrea una textura en el nivel de mipmap especificado.                                           |



 

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

 

 




