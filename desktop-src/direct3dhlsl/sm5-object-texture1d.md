---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 382ac1e436eff4108a2179aeefd4395fbc52c7af304bb719cbadf87a3c1f3d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724876"
---
# <a name="texture1d"></a>Texture1D

Un tipo de textura 1D ([tal como existe en El modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más variables de recursos. Este objeto de textura admite los métodos siguientes, además de los métodos del modelo de sombreador 4.



| Método                                                                  | Descripción                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Cargar**](texture1d-load.md)                                          | Lee los datos de textura.                                                                        |
| [**Operador\[\]**](sm5-object-texture1d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Muestra**](texture1d-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Muestrea una textura después de aplicar el valor de sesgo al nivel de mapa mip.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Muestrea una textura mediante un valor de comparación para rechazar muestras.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Muestrea una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Muestrea una textura en el nivel de mapa mip especificado.                                           |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




