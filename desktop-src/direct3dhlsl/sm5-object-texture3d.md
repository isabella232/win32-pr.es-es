---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL de Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076630"
---
# <a name="texture3d"></a>Texture3D

Tipo Texture3D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso. Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.



| Método                                                                  | Descripción                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Obtiene las dimensiones de recursos.                                                              |
| [**Carga**](texture3d-load.md)                                          | Lee los datos de textura.                                                                        |
| [**MIPS. Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Operador\[\]**](sm5-object-texture3d-operatorindex.md)              | Obtiene una variable de recurso de solo lectura.                                                        |
| [**Ejemplo**](texture3d-sample.md)                                      | Muestrea una textura.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Muestrea una textura en el nivel de mipmap especificado.                                           |



 

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

 

 




