---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL de Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994757"
---
# <a name="texture1d"></a>Texture1D

Un tipo de textura 1D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.



| Método                                                                  | Descripción                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Carga**](texture1d-load.md)                                          | Lee los datos de textura.                                                                        |
| [**Operador\[\]**](sm5-object-texture1d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**MIPS. Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Ejemplo**](texture1d-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Muestrea una textura con un valor de comparación para rechazar ejemplos.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Muestrea una textura en el nivel de mipmap especificado.                                           |



 

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

 

 




